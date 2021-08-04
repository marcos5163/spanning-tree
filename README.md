# spanning-tree
Objects of this class represents the configuration messages received and sent by the bridges

It contains four variables which represent the following values when a bridge sends the message: the bridgeId of the bridge which it assumes is the root, its distance from the root, its bridgeId, the port on which it is sending (which is the LAN name itself)

Any object of this class simulates a bridge in the given network topology.

It contains a map named myPorts whose key is the name of ports and value is a boolean function which indicates whether the port is a designated port or not.

It has a configMessage object named myStatus which represents the current status of the bridge. The four variables of this configMessage object represent the bridgeId of the bridge which it assumes is the root, its distance from it, the next bridge towards the path to the bridge, and the port corresponding to that path which is in fact the root port, respectively.

It contain various queues (priority_queue for receiving configs) to queue up the receiving config messages during spanning tree formation and to queue up the packets during packet transmission.

It contains various public functions to allow spanningTree.cpp to access the values of private variables and some private functions which are kind of some helper functions used to aid the major functions in their execution.

