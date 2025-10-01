# Kenny’s Quinn

Blender addon for animating Unreal Engine 5 Manny & Quinn characters.  
This project provides a custom rigging and animation workflow that makes it easier to create Blender animations compatible with Unreal’s default characters.

---

## Background
As an independent animator and game developer, I often struggled to find a shared workflow between Blender and Unreal Engine.  
Unreal provides Manny/Quinn as default demonstration characters, but creating animations for them in Blender is difficult.

Existing solutions are either outdated or missing features I need.  
So I developed this addon for my own workflow and now share it as a free public test version.

---

## Disclaimer
- This is a **test build**: some features may be incomplete or unstable.  
- I cannot guarantee that every current feature will remain in future releases.  
- The main purpose of this release is to **collect feedback and feature suggestions**.  
- If your suggested feature is accepted, you will receive the official version for free once it is released.  
- Official releases will come with **1 year of free updates** (starting from release date).  

---

## Installation
1. Download the latest release from the <a href="[url](https://wikoding.gumroad.com/l/kennys_quinn_alpha)" target="_blank">Gumroad – Kenny's Quinn Alpha</a> page.  
2. In Blender, go to **Edit → Preferences → Add-ons → Install...**  
3. Select the `.zip` file and enable the addon.  

---

## Usage
A tutorial video will be provided to explain usage in detail.  
For now, please refer to the documentation in this repository and experiment with the rig layers.  

---

## Rig Design
The addon organizes bones into **four layers**, each with a clear purpose:

### Original (Ori)
- Manny/Quinn’s original bones.  
- Cannot be modified.  
- Final animations are baked here.  
- Only these bones deform the mesh.  

### Intermediate (Int)
- Bridges Manny/Quinn’s skeleton with Blender’s bone system.  
- Makes imported bones Blender-friendly.  

### Mechanics (Mch)
- Implements mechanical logic (IK, auto pole, spine bending, etc.).  
- Complex setup is concentrated here.  

### Controllers (Ctl)
- Exposed bones for animators.  
- Designed to be minimal but functional.  
- Uses proxies to avoid dependency cycles.  

---

## Dependency Rules
- Each layer only affects the next layer (Ori ← Int ← Mch ← Ctl).  
- Cross-layer dependencies are forbidden.  
- Cycles are strictly disallowed, except controlled proxies in the Ctl layer.  

---

## Feedback & Issues
- Please open an [Issue](../../issues) for bugs, feature requests, or design discussions.  
- Feedback is especially welcome on rig usability and animation export workflow.  

---

## Roadmap
- Improve IK/FK switching  
- Optimize proxy handling  
- Add more animation-friendly controllers  
- Improve compatibility with third-party animations  

---

## License
This test version is **free to use**, but the final release will be distributed via Gumroad.  
