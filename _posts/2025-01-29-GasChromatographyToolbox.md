---
layout: post
title:  "Web Application for Gas Chromatography Simulation"
date:   2025-01-29
categories: GasChromatographyToolbox Model
---
The interactive web application [GasChromatographyToolbox.org](https://gaschromatographytoolbox.org) brings the simulation of gas chromatography to your browser. This open-source toolbox, built with Julia, offers powerful simulation and calculation capabilities for separation science researchers and practitioners.

## The Demo Application

The web application provides a demonstration of the [GasChromatographySimulator.jl](https://github.com/GasChromatographyToolbox/GasChromatographySimulator.jl) package, allowing users to simulate one-dimensional gas chromatographic separations. This demo specifically features:

- Simulation of 17 different substances on three different stationary phases
- Customizable parameters including:
  - Column length
  - Column diameter
  - Film thickness
  - Carrier gas type and flow
  - Vacuum or atmospheric detector
  - Temperature program

![Screenshot of the GC Simulation](/assets/p4/gc-sim.png)

Users can experiment with these parameters and immediately visualize the resulting chromatogram and peak list in the results section.

## Technical Background

The simulation is powered by [GasChromatographySimulator.jl](https://github.com/GasChromatographyToolbox/GasChromatographySimulator.jl), which serves as the foundation of the [GasChromatographyToolbox](https://github.com/GasChromatographyToolbox/GasChromatographyToolbox). This package, published in the Journal of Open Source Software (2022, [DOI: 10.21105/joss.05755](https://doi.org/10.21105/joss.05755)), implements mathematical models for accurate GC separation predictions. 

The models consists on the flow of the carrier gas through cylindrical columns, a thermodynamic model of the retention of the substances on the stationary phase and diffusion of the substances in the carrier gas. This results in two ordinary differential equations, one for the migration of the substance through the column and one for the development of the width of the peak. These equations are solved numerically.

In previous blog posts I have shown how to [simulate a conventional GC separation]({% post_url 2024-03-13-tutorial_notebook_conventional_GC %}) use the [GasChromatographySimulator.jl](https://github.com/GasChromatographyToolbox/GasChromatographySimulator.jl) package in a Pluto notebook.

The complete toolbox is available on GitHub, embracing open-source principles and encouraging community collaboration.

[Visit the GasChromatographyToolbox on GitHub](https://github.com/GasChromatographyToolbox/GasChromatographyToolbox)

## Why It Matters

This demo version is particularly valuable for:
- Researchers planning GC experiments
- Students learning about chromatographic separation
- Lab technicians optimizing separation methods
- Anyone interested in understanding how different parameters affect GC separation

## Getting Started

You can explore the demo by visiting the [GC Simulation](https://gaschromatographytoolbox.org/gcsim) section of the web application. The interface is designed to be intuitive, allowing users to adjust parameters and observe their effects on the separation process. A selection of the substances is not possible in the demo version.

<div class="clearfix" markdown="1">
<img src="/assets/p4/gc-sim-left-top.png" alt="left top side of the GC-simulation screen" class="align-left" style="width: 45%; margin-right: 15px;">

On the left side of the screen you can set the parameters for the simulation, like length of the column, film thickness or flow rate. These parameters directly influence the separation process and can be adjusted to optimize your chromatographic method.
</div>

<div class="clearfix" markdown="1">
<img src="/assets/p4/gc-sim-left-bottom.png" alt="left bottom side of the GC-simulation screen" class="align-left" style="width: 45%; margin-right: 15px;">

In addition a temperature program with an arbitrary number of steps can be set. The temperature program is a crucial parameter in GC method development, affecting both separation and analysis time.
</div>

<div class="clearfix" markdown="1">
<img src="/assets/p4/gc-sim-run.png" alt="Run Simulation Button" class="align-left" style="width: 45%; margin-right: 15px;">

Clicking on the "Run Simulation" button will start the simulation and after a few seconds the results will be displayed on the right side of the screen consisting of an interactive plot of the chromatogram and a scrollable table of the peak list.
</div>

![right side of the GC-simulation screen](/assets/p4/gc-sim-right.png)

The peaklist shows the retention time, peak width (defined as the standard deviation of the gaussian peak), elution temperature and the resolution between neighboring peaks.

## Future Developments

The demo web application will be expanded to include more features, which are already available in the [GasChromatographyToolbox](https://github.com/GasChromatographyToolbox/GasChromatographyToolbox), especially in the [GasChromatographySystems.jl](https://github.com/GasChromatographyToolbox/GasChromatographySystems.jl) package.

Upcoming demos for:
- GCxGC system simulation
- Flow calculator for complex capillary networks
- Retention parameter estimation

## Take Your GC Method Development to the Next Level

While the demo version showcases the basic capabilities of the GasChromatographyToolbox, the full simulation platform offers much more extensive possibilities for professional applications.

### Professional Method Development
- Custom substance libraries and retention parameters
- Complex multi-dimensional GC systems (GCxGC)
- Advanced flow calculations for complex networks of columns
- Integration with your existing workflow

### Educational Implementation
Are you an educator or training provider? The GasChromatographyToolbox can be customized for educational purposes:
- Interactive learning modules
- Student-friendly interfaces
- Practical exercises and assignments
- Virtual lab experiences

### Custom Solutions
Looking for specific features or implementations? The toolbox can be adapted to meet your unique requirements:
- Custom user interfaces
- Specific industry applications
- Specialized simulation parameters
- On-premise deployment

## Let's Discuss Your Needs

Whether you're interested in:
- Professional method development solutions
- Educational implementations
- Custom adaptations
- Training and support

I'm here to help turn your ideas into reality.

📧 Contact me at: [info@janleppert.org](mailto:info@janleppert.org)

[Visit my consultant page](https://janleppert.de/consultant) to learn more about my work in scientific software development and analytical chemistry solutions.


