---
layout: archive
title: "For Scientists"
permalink: /sdssmgii/
author_profile: true
header:
  overlay_image: galaxy.jpg
---

{% include base_path %}

# Absorber Catalogs & Tools

## qsoabsfind
I developed an automated absorber detection pipeline, [**qsoabsfind**](https://github.com/abhi0395/qsoabsfind), which uses a matched-kernel convolution technique and adaptive signal-to-noise criteria.  
The pipeline is designed for high-performance analysis and can run in parallel on thousands of quasars simultaneously, significantly reducing the absorber search time.  

- Latest release: [v1.0.5](https://github.com/abhi0395/qsoabsfind/releases)  
- Features: multi-ion support (Mg II and C IV), robust absorber selection, equivalent width measurements and error estimations.

---

## Mg II / Fe II Absorber Catalog
Using a preliminary version of *qsoabsfind* (developed during my PhD), I processed all quasars from SDSS DR16 to build the largest [**Mg II / Fe II catalog**](https://www.mpa-garching.mpg.de/SDSS/MgII) to date, containing ~160,000 systems.  
This catalog is widely used for CGM–absorber cross-correlation studies and large-scale structure analysis. 

---

## C IV Absorber Catalogs
As part of DESI, I developed the first large-scale **C IV absorber catalog** based on DESI Year 1 quasar spectra.  

- **C IV Absorber Catalog (DESI DR1):** [DESI Data Access](https://data.desi.lbl.gov/doc/releases/dr1/vac/civ-absorber/)  
- **On GitHub:** [Github Link](https://github.com/abhi0395/desi-dr1-civ)  

This catalog contains over 33,000 CIV systems, enabling statistical measurements of absorber incidence, equivalent width distributions, and cosmic mass density evolution.  

*Future Work:* A DR2 C IV absorber catalog will be released in future — stay tuned, as I will share the link here once available.  

# Redshift Fitter for Large Surveys

In my recent work [Anand et al. 2024](https://arxiv.org/abs/2405.19288), I developed a computationally efficient galaxy archetype-based redshift estimation and spectral classification method for the [Dark Energy Spectroscopic Instrument (DESI)](https://www.desi.lbl.gov/).  
This approach builds upon and extends the [redrock](https://github.com/desihub/redrock) pipeline.

**Highlights:**
- Refits spectra with physical galaxy archetypes + additional terms to absorb data-reduction defects.  
- Improves redshift success rates and reduces catastrophic failures by 10–30% for galaxy targets.  
- Addresses limitations of classic PCA models (e.g., unphysical modeling, overfitting).  
- Generic method that can be extended to other large surveys like [WEAVE](https://www.ing.iac.es/astronomy/instruments/weave/weaveinst.html), [WAVES](https://wavesurvey.org/), and [PFS](https://pfs.ipmu.jp/)

