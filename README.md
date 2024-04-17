NAT Check

Version 3, with UDP and TCP support

Check Your Network Address Translator
for Compatibility with Peer-to-Peer Protocols

In order to validate Nat Traversal capability, this project includes both natserver.c and natcheck.c

For specific details, please see https://midcom-p2p.sourceforge.net

To validate, you will need to change SERV1, SERV2, and SERV3 in the source code.
Next, build server with the following:
cd natchecker/server
cmake -B . && make

To build the client, follow the same instruction:

cd natchecker/client
cmake -B . && make

Next, you will need to start three servers and one client

./natserver -v 1
./natserver -v 2
./natserver -v 3

./natcheck -v

Natcheck will output the result on the test to vaidate whether Nat Traversal is possible in your paticular environment.