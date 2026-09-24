# Communication between Unity Scripts

At the core of programming is communication between different parts of an overall project. For example...
- we have prefabs which aare created and/or stored in our poroject which we want to instantiate (e.g. the bomb prefab)
- the plane decides it wants to drop a bomb it needs to inform the "BombSlots"
- the Camera needs to follow the plane

Depending on the circumstance, different ways of communicating between (typicaally) different scripts may be used.

## The Setup

Sometimes only information about position, or orientation might be required, and sometimes we may need more specific information to be passed back and forth between scripts. How the link is made defines everything. The easiest way is through a [public variable](Variables_in_C_Sharp.md)

### Public Variables in Unity

Advantages:
-Easiest, intuitive
-Can be "baked" into prefabs 

Disadvantages
-Wont work for Insatantiated Game objects or if you have a lot of objects in a given scene you'd like to link

#### How?

If  a script is to be linked to another object throughh a variable, a public variable is declared, which becomnes visible on the INspoector in the unity editor.  The object you'd like to link can be draagged onto the appropriate slot in the inspector.

E.g. 

In our game, we wished to Instantiate bombs, to do this we created a Bomb Prefab.  The plane script had a public variable theBombCloneTemplate

```csharp
public class RS_PlaneControl : MonoBehaviour
{
    float pitchingSpeed = 45f;  // Speed in degrees per second for pitching
    private float rollingSpeed = 45f;
    internal Vector3 velocity, acceleration;
    private float thrustValue = 20f;
    private float gravity = 9.81f;
    float drag = 1;

    public GameObject theBombCloneTemplate;

    int NextBombSlotIndex = 0;
```
