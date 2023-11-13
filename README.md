# NS2-31-Channel-Assignment
Random Channel Assignment

This repository assign random channels to cognitive nodes. On RREQ random channels are generated and appended with RREQ. The nodes on the path create Reverse routes with these channels and save the channel entry in Routing Table. 
Later on, on reception of RREP from a node, each node creates the Forward Route entry. These entries are created from getting the channel in reverse entry on a node.
To run this code, simply Install NS2.31 with CRCN patch (attached with code) , and replace "aodv" "common" and "mac" folder of default implementation with the folders of this reporistory and recompile.

####How to chek the code is working
run the code with a simulation script, a sample scipt also attached. It will generate a lot of log messages, you need to filter two messages, one is related to RREQ, RREP and second is related to Packet  Foward.
For Example the output is logged in file name "log" ,then run these two grep commands
rep "RREQ" log > log2
grep "FWDPKT" log > log3


Due to restriction of file size, I have only uploaded the files which are needed to make these changes affective
It  will log reuiqred data, simply analyse it and you will find every thing :)

