# Communication between Unity Scripts

At the core of programming is communication between different parts of an overall project. For example...
- we have prefabs which aare created and/or stored in our poroject which we want to instantiate (e.g. the bomb prefab)
- the plane decides it wants to drop a bomb it needs to inform the "BombSlots"
- the Camera needs to follow the plane

Depending on the circumstance, different ways of communicating between (typicaally) different scripts may be used.

## The Setup

Sometimes only information about position, or orientation might be required, and sometimes we maay need more specific information to be passed back and forth between scripts. How the link is made defines everything. The easiest way is through a [public variable](.  

