Node UDP Hole punching
=========================

Introduction
-------------------------

In this experiment it is attempted to use the UDP Hole punching technique to
initiate a connection between two clients behind NAT (without port forwarding).

Goals
-------------------------

The first goal is to create a simple script that allows sending UDP packets 
from client to client, in both directions (current state).
Future goals include the development of a library that offers this method in a
more extensible manner.

Usage
-------------------------
A public machine acts as a rendezvous server (running rendezvous.js), two
clients behind NAT start client.js.
A client can ask the rendezvous server to help them him to connect to another
client using the TCP hole punching procedure.

1. Server
    node rendezvous.js

2. Client A
    node client.js [server] [nameA]

3. Client B
    node client.js [server] [nameB] [nameA]


