# Cita417Lab5
Youtube Video Link - https://www.youtube.com/watch?v=05zYNpodtqY

This project demonstrates how content-aware tuning in Unreal Engine can improve runtime performance. A large number of static cubes and a Cascade fire particle system were used to create a baseline “stress” environment. Two simple optimizations were applied to show measurable FPS improvement.

## Scene Setup (Before Optimization)  
- 1,000 cubes placed throughout the map  
- Cascade fire particle effect in the scene  
- FPS and actor count visible on-screen  
- No gameplay logic or triggers — the scene loads and immediately displays the stress conditions  

## Optimizations Applied  

### **1. Disabled Collision on All Cubes**  
The cubes are purely decorative, so physics/collision was unnecessary.  
Disabling collision reduces CPU physics cost across all 1,000 cubes.

### **2. Removed Fire Particle System**  
The Cascade fire effect generated significant GPU and overdraw cost.  
Removing it for the after-test results in a cleaner and lighter scene.

## How to Reproduce  
1. Open the project in Unreal Engine.  
2. Load the main map containing the cube field.  
3. Ensure the FPS overlay is active.  
4. Observe performance with and without the fire effect / collision disabled.  
5. Compare FPS directly, as shown in the demo video.
