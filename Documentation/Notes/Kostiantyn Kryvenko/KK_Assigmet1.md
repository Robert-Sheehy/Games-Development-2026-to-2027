
## Ground Raycast Aim Reticle 

## Overall Idea
For this purpose I will create a folder called KK_raycastDev scene called KK_raycastScene in this scene I'm going to use prefab of a plane called "Plane Prefab" which will contain a plane model and 4 slots for bombs, I will have prefab of a bomb called "Bomb prefab". In plane prefab I'll have a for bomb slots, script responsible for moving, and camera called "KK_PlaneControl" attached to a plane model, and  each bomb slot will have its own script called "KK_BombSlot" responsible for initializing bombs in correct places.
At the scene I will locate Reticles on the floor, make a script that will drop bombs according to the speed of the plane  
