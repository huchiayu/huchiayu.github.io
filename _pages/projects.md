---
layout: page
title: Research
permalink: /research/
#description: A growing collection of your cool projects.
nav: true
nav_order: 3
display_categories: [work, fun]
horizontal: false
---


The overarching theme of my research is
understanding how galaxies form and evolve using **high-fidelity** hydrodynamical simulations,
with an emphasis on **interstellar chemistry**.
Understanding galaxy formation requires a profound knowledge of
*how gas, molecules, and dust flow into and out of galaxies*.
Gas radiatively cools, gravitationally collapses into molecular clouds and forms stars,
which in turn inject energy, momentum, and metals back into the interstellar medium (ISM) via stellar feedback,
driving turbulence,
destroying clouds,
and launching galactic winds.
The ISM and winds are both **multiphase** in nature,
and our knowledge of them comes from **multiwavelength** observations.
Therefore,
their **chemical properties**
are of fundamental importance
as they dictate the observational tracers of different phases.
My research aims to answer the following questions:

 - What shapes the distributions of molecules and dust in different galaxies? How do they trace the cold, star-forming clouds?

 - What is the origin of molecular winds (entrained v.s. in-situ)? How do molecules and dust survive in hot medium? How do different observational diagnostics trace the winds?

Revolutionary observatories such as
ALMA, JWST, and SKA
will provide exquisite multiwavelength data in the coming years,
and it is timely to design and perform simulations
that can reliably make predictions of these observables.
While modern cosmological simulations have made significant progress in forming realistic galaxies,
they still (and will remain to) lack the required resolution to capture
the multiphase ISM structures and the feedback processes
In light of this, **high-fidelity** simulations,
where small-scale processes are resolved and simulated "from first principles",
offer a promising way forward.


## Co-evolution of the interstellar dust and chemistry in low-metallicity dwarf galaxies

Nearby dwarf irregular galaxies
are ideal laboratories for studying the ISM at low metallicity,
which is expected to be common for galaxies at very high redshift
that will be observed by the James Webb Space Telescope.
In [this paper](https://ui.adsabs.harvard.edu/abs/2023arXiv230105247H/abstract),
I conducted the first high-resolution (~0.2 pc)
hydrodynamical simulations of an isolated low-metallicity dwarf galaxy
coupled with a time-dependent chemistry network and a dust evolution model.
I show that dust growth in dense gas is required to reproduce the observed CO luminosity
as otherwise CO would be completely photodissociated.
In contrast, the H2 abundance is extremely small and is insensitive to dust growth.
Observationally inferred dust-to-gas ratio is thus underestimated
if adopting the metallicity-dependent CO-to-H2 conversion factor.
The galactic outflows are 20% - 50% dustier than the ISM,
providing a possible source for intergalactic dust.

<br/><img src='/assets/img/old_pics/chem_dust_coevo.png' width="800">


## Code Comparison in Galaxy Scale Simulations with Resolved Supernova Feedback: Lagrangian vs. Eulerian Methods

Galaxy scale simulations with parsec-scale resolution have become feasible in recent years.
Motivated by its increasing importance,
I led a code comparison project in
[this paper](https://ui.adsabs.harvard.edu/abs/2022arXiv220810528H/abstract)
as part of the [SMAUG collaboration](https://www.simonsfoundation.org/flatiron/center-for-computational-astrophysics/galaxy-formation/smaug/).
We show that
Lagrangian codes show significantly burstier star formation, larger supernova-driven bubbles,
and stronger galactic outflows compared to the Eulerian code.
This is caused by the difference in the spatial and temporal clustering of supernova events,
as gas in Lagrangian codes collapses to much higher densities than in Eulerian codes.


<br/><img src='/assets/img/old_pics/fof_scatter_all.png' width="800">




## H2, CO and the CO-to-H2 conversion factor (X_CO) in a self-regulated interstellar medium

In typical star-forming galaxies with solar metallicity, CO emission is a robust and the most
widely used tracer for the invisible H2 gas where star formation occurs. However, at low metallicites
where dust shielding is ine cient, the UV radiation penetrates deeper into the clouds and
photodissociates CO, making it a poorer tracer.

In [this paper](https://ui.adsabs.harvard.edu/abs/2021ApJ...920...44H/abstract),
I conducted simulations of the feedback-regulated ISM in the "stratified disk" setup with
an unprecedented dynamical range both temporally and spatially, running for 500 Myrs
and reaching sub-parsec (~0.2 pc) spatial resolution (which has previously only been achieved
with the "zoom-in" techniques and was limited to a few Myrs). The long time period allows me
to sample a large ensemble of clouds while the sub-parsec resolution is critical for resolving the
dense and compact cores where CO lives, especially at low metallicities. In addition, I explored
a large metallicity range (from 0.1 to 3 Z_solar), covering the low-metallicity regime typical
in dwarf galaxies for the first time in SN-resolved stratified disk simulations.
I showed that at low metallicities, the steady-state model substantially
over-produces H2 but not CO, because H2 is
limited by the available time for it to form in the dynamic ISM.

<br/><img src='/assets/img/old_pics/chem_maps.png' width="800">

In [this paper](https://arxiv.org/abs/2201.03885),
I constructed synthetic maps of CO(1-0) and CO(2-1) using the radiative transfer code RADMC-3D.
I showed that on parsec scales, X_CO varies by orders of magnitude from place to place,
primarily driven by the transition from atomic carbon to CO, and it drops to the Milky Way value
once dust shielding becomes effective, independent of metallicity.
X_CO is a multi-variate function of CO intensity, metallicity and beam size.
Describing X_CO as a one-parameter function of metallicity is
incomplete as different telescopes measure X_CO in different regimes of the parameter space,
Taking all three variables into account allows us to better infer the H2 mass.

<br/><img src='/assets/img/old_pics/XCO_maps_pix.png' width="800">


## Dust destruction in a multiphase interstellar medium

Dust is an important element of the ISM: it provides a major heat source via the photoelectric
effect and triggers H2 formation and all the subsequent chemistry. However, most simulations treat
it as a constant field, while a few simulations that include dust evolution only do so in a sub-grid
fashion. In [this paper](https://ui.adsabs.harvard.edu/abs/2019MNRAS.487.3252H/abstract),
I have developed an ab initio scheme to simulate dust sputtering by SN blastwaves,
following the dust dynamics governed by direct collisions, plasma drag and betatron acceleration.
With it, I have conducted the first hydrodynamical simulations of dust destruction in an
SN-driven multiphase ISM in the solar neighbourhood and quantified the destruction timescale.

<br/><img src='/assets/img/old_pics/DGRmaps.png' width="800">

## A priori validation of subgrid-scale models for astrophysical turbulence

Turbulence is ubiquitous in astrophysics. Resolving the full dynamical range of turbulence cascade
is computational formidable, and turbulent mixing on the sub-grid scales is often treated as a
diffusion process, either explicitly or implicitly.
In [this paper](https://ui.adsabs.harvard.edu/abs/2020ApJ...900...29H/abstract),
I ran both the isothermal turbulent box
and the wind tunnel simulations, and I showed that the instantaneous turbulent transport is highly
anisotropic and hence isotropic diffusion is a poor approximation. Instead, a gradient-based
model based on Taylor expansion predicts the sub-grid fluxes much more accurately.

<br/><img src='/assets/img/old_pics/blob_sgs.png' width="800">

## Supernova-driven winds in dwarf galaxies

SN-feedback is thought to be the primary mechanism to drive galactic winds.
In [this paper](https://ui.adsabs.harvard.edu/abs/2019MNRAS.483.3363H/abstract),
I quantified
the fluxes of mass, momentum, energy and metals of the galactic winds in dwarf galaxies as
a function of radius. I showed that the predicted winds are much weaker than what
cosmological simulations commonly adopt, with a mass loading factor around 3 to 5.
In addition, the widely-used momentum-based sub-grid model for SN feedback does not
help drive winds, as winds are driven by thermal pressure rather than momentum.

<br/><img src='/assets/img/old_pics/dwf_winds.png' width="800">

## Stellar feedback in dwarf galaxies: supernovae versus photoelectric heating

Dwarf galaxies form stars ine ciently, with their depletion time comparable to the Hubble
time. The origin of their long depletion times is still unclear.
In [this paper](https://ui.adsabs.harvard.edu/abs/2017MNRAS.471.2151H/abstract),
I developed a novel scheme to form and follow individual massive stars
in galactic-scale simulations for the first time. I showed that SN-feedback
is the primary mechanism (rather than photoelectric heating) for suppressing star
formation in dwarf galaxies. The predicted ratio of C+ emission to dust continuum matches
observations of nearby dwarf galaxies only when SN-feedback is included.

<br/><img src='/assets/img/old_pics/dwf_vG0.png' width="800">

## Star formation and molecular hydrogen in dwarf galaxies: a non-equilibrium view

The amount of molecular hydrogen (H2) in dwarf galaxies is poorly constrained
as the main tracer, CO, is often too
faint to be detected. In [this paper](https://ui.adsabs.harvard.edu/abs/2016MNRAS.458.3528H/abstract),
I conducted the first SN-resolving, galactic-scale simulation with sub-pc resolution.
I showed that the correlation between H2 and star formation
breaks down at low metallicity (Z = 0.1 Z_solar ) on galactic scales, casting doubt on the
applicability of the widely adopted H2-based star formation recipes in cosmological simulations and
semi-analytic models for low-metallicity environments commonly found in high-redshift galaxies.

<br/><img src='/assets/img/old_pics/dwf_H2.png' width="800">

## SPHGal: smoothed particle hydrodynamics with improved accuracy for galaxy simulations

SPH is a very popular numerical method of hydrodynamics in astrophysics thanks to its inherently
adaptive spatial resolution. However, traditional SPH has severe difficulties to properly model
fluid mixing and suffers from a slow convergence rate.
In [this paper](https://ui.adsabs.harvard.edu/abs/2014MNRAS.443.1173H/abstract),
I have developed an SPH scheme with
a noval limiter for the artificial viscosity and thermal conduction, implemented it in
the Gadget-3 code, and found remarkable improvements in both fluid mixing and shock capturing in the
validation tests. This SPH scheme has been used in many of my papers and by my collaborators.

<br/><img src='/assets/img/old_pics/sphgal_sedov.png' width="800">
