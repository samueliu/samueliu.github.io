---
layout: single
title: LVAD Impeller Design
permalink: /portfolio/lvad-impeller/
header:
  overlay_image: /images/impeller2.png # Add the path to your splash image
  overlay_filter: 0.5 # Optional: Adjust the filter opacity for better title visibility
  overlay_full: true  # Makes the header full-width
  actions:
---

_This was a project done with a team at University College London for the manufacturing module._

We designed an impeller to be used for a left-ventricular pump, with full considerations for DFM, materials selections, production methods, cost, and lifecycle analysis. Below is a table used for initial engineering criteria, as we optimized blade number, height, slope, and angle for impeller efficiency.

<div style="text-align: center;">
  <img src="/images/stats.png" alt="impeller table" style="max-width: 80%; height: auto; border-radius: 10px;">
  <p><em>Table showing chosen design and parameters</em></p>
</div>

The resulting CAD model was created to be 3D printed as a proof-of concept.

<div style="text-align: center;">
  <img src="/images/impeller.png" alt="impeller" style="max-width: 60%; height: auto; border-radius: 10px;">
  <p><em>CAD model for one of the final chosen designs</em></p>
</div>

We then made decisions on a material selection software given our functional requirements, and opted for a stainless steel suitable for long-term biological applications over other options deemed to be more expensive or insufficient.

<div style="text-align: center;">
  <img src="/images/materials.png" alt="materials selection" style="max-width: 75%; height: auto; border-radius: 10px;">
  <p><em>Graph showing minimum critera and cost compared to different materials</em></p>
</div>

After determining the best course of manufacturing to be machining given the tight tolerances we calculated, our design was tested along with the rest of the module in a machine measuring flowrates to observe efficiency.


<div style="text-align: center;">
  <img src="/images/impeller_test.png" alt="test rig" style="max-width: 75%; height: auto; border-radius: 10px;">
  <p><em>Testing rig used for impeller design</em></p>
</div>

**Skills Used:**
- CAD
- Optimization of Parameters
- Design for Manufacturing
