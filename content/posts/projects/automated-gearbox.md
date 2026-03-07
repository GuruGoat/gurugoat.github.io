---
title: "Automated Gearbox Design"
date: 2023-06-15T00:00:00-00:00
description: "Custom high-torque gearbox for robotic arm application"
#hero: /images/posts/gearbox-hero.jpg
tags: ["CAD", "FEA", "Robotics", "SolidWorks", "Manufacturing"]
categories: ["Projects"]
---

## Project Overview

Designed and prototyped a compact, high-torque planetary gearbox for a 6-DOF robotic arm requiring precise motion control with minimal backlash.

#{{< img src="/images/posts/gearbox/assembly-render.jpg" align="center" title="Gearbox Assembly">}}

Or use pCloud-hosted images:

#![Gearbox CAD Assembly](https://filedn.com/yourpcloud/gearbox-cad-render.jpg)
![Gearbox CAD Assembly](https://e.pcloud.link/publink/show?code=XZd6v3ZIHEHEW1Oj5hCjPa8YVESXmBlhYky)
*SolidWorks assembly render showing internal gear train*

## Design Requirements

The project specifications were:

- **Torque Output**: 50 Nm minimum
- **Gear Ratio**: 20:1 reduction  
- **Backlash**: <0.5° maximum
- **Form Factor**: Must fit within Ø100mm envelope
- **Efficiency**: Target >90%
- **Weight**: Minimize while maintaining strength

## Design Process

### Initial Concept

I evaluated several gear train configurations:

1. **Planetary gear system** (selected)
   - Compact form factor
   - High torque density
   - Even load distribution

2. Harmonic drive alternative
   - Excellent for zero backlash
   - More expensive to manufacture

3. Traditional spur gear train
   - Simpler but larger package size

The planetary configuration offered the best balance of compactness, efficiency, and manufacturability for this application.

### CAD Modeling

{{< vs 3 >}}

#![Exploded View](https://filedn.com/yourpcloud/gearbox-exploded.jpg)
#*Exploded assembly view showing component relationships*

Key design features:

- **Integrated planet carrier** with precision bearing mounts
- **Hardened steel ring gear** press-fit into aluminum housing
- **Custom sun gear** with integrated motor coupling spline
- **Three planet gears** for load distribution (120° spacing)

All components modeled in SolidWorks with full parametric control for easy design iterations.

### FEA Analysis

Static structural analysis was performed to validate the design under maximum loading conditions.

#{{< img src="/images/posts/gearbox/fea-stress.jpg" align="center" title="FEA von Mises Stress Analysis">}}

**Analysis Results:**
- Maximum stress: 285 MPa (well below 7075-T6 yield of 503 MPa)
- Safety factor: 1.8
- Maximum deflection: 0.08mm at max torque
- No stress concentrations in critical areas

The analysis confirmed the design would handle specified loads with adequate safety margin.

## Manufacturing & Prototyping

### Machining Process

Components were manufactured using a combination of methods:

**Ring Gear:**
- Material: 4140 alloy steel
- Rough machining on CNC mill
- Heat treatment to HRC 58-62
- Finish grinding for final dimensions

**Planet Gears:**
- Wire EDM cut from S7 tool steel
- Hobbed teeth for precision
- Nitrided surface for wear resistance

**Housing:**
- 6061-T6 aluminum
- 4-axis CNC machining
- Anodized finish

### Manufacturing Video

{{< vs 2 >}}

<video width="100%" controls>
  #<source src="https://filedn.com/yourpcloud/gearbox-machining.mp4" type="video/mp4">
  <source src="https://e.pcloud.link/publink/show?code=XZ4Ev3ZHqdKwBfjopbmdPfSbo91Njy8tRfV" type="video/mp4">
  Your browser doesn't support video playback.
</video>

*Time-lapse of housing being machined on Haas VF-2 CNC mill*

## Testing & Validation

### Test Setup

Built a custom test rig to measure:
- Torque transfer efficiency
- Backlash under load
- Temperature rise during operation
- Noise levels

#![Test Rig](https://filedn.com/yourpcloud/gearbox-test-rig.jpg)
#*Dynamometer test rig with torque sensors and data acquisition*

### Performance Results

The prototype exceeded all design specifications:

| Parameter | Target | Achieved |
|-----------|--------|----------|
| Efficiency | 90% | 92% |
| Backlash | <0.5° | 0.3° |
| Max Torque | 50 Nm | 55 Nm |
| Weight | - | 1.2 kg |
| Operating Temp | - | 45°C max |
| Noise Level | - | 68 dB |

### Load Testing Video

#<video width="100%" controls>
#  <source src="https://filedn.com/yourpcloud/gearbox-load-test.mp4" type="video/mp4">
#</video>

*Gearbox under full-load testing at 3000 RPM input speed*

## Results & Key Learnings

### Project Achievements

✓ **Met all design requirements** with margin to spare  
✓ **30% more compact** than commercial alternatives  
✓ **15% cost reduction** vs off-the-shelf solutions  
✓ **Successfully integrated** into final robot design  
✓ **Zero failures** during 1000-hour endurance testing  

### Technical Insights

**What Worked Well:**
- Planetary design delivered excellent torque density
- FEA validation reduced prototype iterations significantly  
- Integrated bearing mounts simplified assembly
- Heat treatment process delivered consistent hardness

**Challenges Overcome:**
- Initial backlash exceeded spec - resolved with tighter tolerances on planet carrier
- Assembly required custom tooling for press-fitting ring gear
- Balancing cost vs performance in material selection

**Key Takeaways:**
1. **Design for Manufacturing (DFM)** - early consultation with machinist saved rework
2. **Tolerance stacking analysis** critical for backlash management
3. **Testing under real conditions** revealed thermal issues not seen in simulation
4. **Documentation discipline** - parametric CAD made design changes much easier

## Technical Specifications

**Materials Used:**
- Ring Gear: 4140 Steel (HRC 58-62)
- Planet Gears: S7 Tool Steel (nitrided)
- Sun Gear: 4340 Steel
- Planet Carrier: 7075-T6 Aluminum
- Housing: 6061-T6 Aluminum (anodized)

**Dimensions:**
- Overall: Ø95mm × 65mm length
- Weight: 1.2 kg
- Mounting: Standard NEMA 23 motor interface

**Performance:**
- Gear Ratio: 20:1
- Input Speed: 3000 RPM max
- Output Torque: 55 Nm continuous, 75 Nm peak
- Efficiency: 92%
- Backlash: 0.3° (10 arcminutes)
- Design Life: 10,000 hours

---

## Files & Resources

**CAD Files**: Available upon request  
#**FEA Reports**: [Download PDF](/files/gearbox-fea-report.pdf)  
#**Technical Drawing**: [View PDF](/files/gearbox-drawing.pdf)  

---

*This project was completed in collaboration with [University/Company Name] for robotics research applications.*
