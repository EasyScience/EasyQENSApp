# Roadmap for EasyQENS

This documents the planned roadmap for the EasyQENS project (containing both [EasyQENSApp](https://github.com/easyScience/EasyQENSApp) and [EasyQENSLib](https://github.com/easyScience/EasyQENSLib)) between now and the start of 2027. 
Certain tasks may depend on other Easy-family projects (in particular EasyCore) which will be be noted, where relevant. 

*Note that this chart should only be used to understand the planned features and a vague timeline for EasyQENS development*.

```mermaid
gantt
    title EasyQENS Roadmap Mar 2023-Jan 2027
    dateFormat  YYYY-MM
    axisFormat  %Y-%m
    todaymarker off

    section General
    Mockup GUI of desired features :a1, 2024-03, 4w
    %% Resolution smearing :a2, after a1, 8w
    %% Resolution smearing :a2, 2024-01, 8w
    %% Video Tutorials :a3, after a2, 8w
    %% File IO :a4, after c2, 16w
    Ready for real users: milestone, m1, 2024-12, 2min

    section Visualization
    Load simple data :b1, 2024-03, 4w
    Basic raw data plot controls :b2, after b1, 8w
    Advanced raw data plot controls: b3, after m1, 8w
    Basic fit result plot controls: b4, after b2, 8w
    %%Bayesian analysis :b3, 2025-01, 30w
    %%ESS integration :b2, after b3, 10w
    %%Ready for first ESS instruments :milestone, m2, 2025-11, 2min
    %%ESS Start of User Operation :milestone, m3, 2026-11, 2min

    section Raw data fitting
    Integrate QENSLibrary :c1, after b1, 2w
    Fit resolution function to simple functions :c2, after c1, 4w
    Fit resolution function to spline: c3, after m1, 4w
    Fit data to sum of elastic and Lorentzian: c4, after c2, 4w
    Convolute spline resolution with model: c6, after m1, 4w
    Make it easy to fit several Q :c5, after c4, 4w
    Make it easy to fit several T and samples :c6, after c5, 4w
    %%Magnetism support :c1, after m1, 40w
    %%Spin asymmetry and polarisation analysis :c2, after m2, 30w

    section Results fitting
    Fit widths to basic diffusion models: d1, after b4, 4w
    %%# Bilayer item :d1, 2024-01, 8w
    %%Material gradient :d2, after b1, 7w
    %%Mixed surfactant layer :d3, after d2, 8w
    %%Bilayer with embedded protein :d4, 2025-07, 16w
    %%Mixed bilayer item :d5, after c2, 8w

    section Advanced features
    Data correction, absorption, sample holder :e1, after m1, 12w
    Basic inelastic scattering :e2, after m1, 12w
    Automate resolution fit :e3, after m1, 12w
    Automate guesses for fits :e4, after m1, 12w
    Fit data directly to diffusion model: e5, after m1, 12w
    Generate LaTeX report of experiment: e6, after m1, 12w    
    Video tutorials :e7, after m1, 12w
    Sample project files :e8, after m1, 12w
    
```

Above we include a Gantt chart showing an early draft of the roadmap. 
Each epic in this chart can be correlated with a heading below which details it. 
In time, each epic will be populated with a series of issues relating to the part of the Easy-family of projects that it pertains to.
Issues that are general to EasyQENS (i.e. those related to interaction with the userbase) will be defined as EasyQENSApp issues.  

## Details 

### General


### Raw data fitting
Functionality to fit the resolution function and raw data convolved with the resolution

### Results fitting
The fit parameters from the raw data fits can be fitted to various models, which is the goal of this epic.

### Video tutorials

Short video tutorials to accompany example projects.
These can be hosted on YouTube or similar and linked to from EasyQENS.org.

### Advanced features
These are features that are not necessary for the first release of EasyQENS, but are desired down the rote. 

### ESS integration

This means integration with the SciCat data catalogue, such that ESS data can be easily loaded to EasyQENS. 
Additionally, it will include the use of `scipp` as a data storage object and `plopp` plotting functionality. 

- [Intraction with SciCat data catalogue](https://github.com/easyScience/EasyReflectometryLib/issues/48)
- [SciCat GUI integration in Experiment pane](https://github.com/easyScience/EasyReflectometryApp/issues/110)
- [Integrate orsopy metadata into scipp object](https://github.com/easyScience/EasyReflectometryLib/issues/49)
- [Use scipp for data storage in the application](https://github.com/easyScience/EasyReflectometryApp/issues/111)
- [Use plopp as a plotting engine in a Jupyter Notebook](https://github.com/easyScience/EasyReflectometryLib/issues/50)
- [Use plopp as a plotting engine in the application](https://github.com/easyScience/EasyReflectometryApp/issues/112)


