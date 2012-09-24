jumpgraph
=========

An interpreter of graphs as algorithm 

Interpreter out line
--------------------

  * Load a graph as a network of instructions
  * Load a given data environment (could be empty)
  * Sets the current_node to the first node in the instruction graph
    * visit all "get" edges and revieve data from them.
    * run the core process of the current node (might include going to step A).
    * visit all "set" edges and write data to them.
    * evaluate "transition" edges and follow the first one that passes the guard.
    * repeat the above with the new current_node... until a terminal node is found or no out transitions exist.
  * Return any data that is marked for return to a calling (outer) environment.
  
An instruction graph is able to express any algorithm. 
This interpreter executes the instruction graphs algorithm within a given environment.
  
