---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
header:
  overlay_image: galaxy2.jpg
---

{% include base_path %}


# **Overview**

Broadly speaking, there are two main themes of my research:

  * **[Galaxy formation and evolution:](#galaxy-formation-and-evolution)** I study how galaxies form and evolve using observational tools. Understanding the physical processes that form the galaxies and set their evolution has been one of the central problems in astronomy. With the advent of advancements in computer simulations combined with powerful telescopes, we have slowly started to uncover the hidden mysteries of our vast universe. Recent large-scale cosmological simulations have revealed that the galaxies are surrounded by a diffuse gaseous halo, known as the [circumgalactic medium (CGM)](https://www.annualreviews.org/doi/10.1146/annurev-astro-091916-055240). Understanding the interplay between different gas flows (outflows and inflows, also known as the cosmic baryon cycle) in this invisible medium is the key to a clear and accurate picture of the fate of galaxies. In a broader sense, I want to understand the -
    * physical processes that govern the formation and evolution of galaxies and their environment.
    * the complex nature of the gas flows in the CGM and how they depend on and impact the galaxy properties and its environment.
    * nature and evolution of metals in the universe using absorption line studies.

  * **[Data science methods:](#data-science-methods)** Astronomy is an observational science that relies on extensive data gathered from telescopes worldwide to study celestial objects. Analyzing these vast amounts of data requires a wide array of methods and techniques to extract scientific insights. I am deeply interested to developing and learning new data analysis tools and incorporating them into my research. I utilize classical machine learning and statistics-based methods to create efficient algorithms for modeling astronomical spectra and measuring their physical properties. I am a regular developer or contributor to several GitHub codebases -
    * [qsoabsfind](https://github.com/abhi0395/qsoabsfind): Absorption feature finder in astronomical spectra (_Developer_)
    * [redrock](https://github.com/desihub/redrock): Spectral fitting module for DESI (making largest 3D map of the universe) (_Contributor_)
    * [desihub](https://github.com/desihub/): Public code associated with the [Dark Energy Spectroscopic Instrument (DESI)](https://en.wikipedia.org/wiki/Dark_Energy_Spectroscopic_Instrument) (_Member_)

## **<u>Galaxy formation and evolution</u>**

### **Cosmic Baryon Cycle**

In simple terms, the ["cosmic baryon cycle"](https://arxiv.org/abs/2011.01935) is very similar to how evaporation and rain work on the earth. We all know that the sun heats the water on Earth, which evaporates and goes up and condenses to form clouds that shower rain on Earth. This process continues, and we call it the water cycle in hydrology. Similarly, the pristine gas (mostly hydrogen and helium) is accreted (also known as the inflow) by the galactic halo (CGM), where it forms gaseous clouds (a very complex physical mechanism) which falls on the galactic disk where it is turned into stars. Finally, these stars release a lot of energy via supernovae or stellar winds, which kick gas out of the galaxy into the halo (CGM) (known as the galactic outflows, see Figure below, right). This process also makes the CGM very multiphase, where gases with different temperatures and densities compete. Will the galaxy continue getting fuel and forming new stars, or will it stop forming stars, depending on the balance between these gas flows? However, predicting or fully understanding the fate of galaxy formation is very challenging!

<figure>
<p style="text-align: center;">
<figcaption>Gas flows in the CGM (simulation from Lochhaas et al. 2021, left and Peeples et al. 2015, right).</figcaption>
</p>
<p float="left">
  <img src="/images/cgm/cgm_flows.jpg" style="width:50%; border:1;">
  <img src="/images/cgm/cgm_ARAA_Nature15_peeples.jpg" style="width:45%; border:1;">
</p>
</figure>

### **Multiphase Circumgalactic Medium in Observations**

As described above, the CGM plays a pivotal role in galaxy formation, but it is very challenging to study it observationally. The CGM is very diffuse (having low densities, $n\sim 10^{-3} \,cm^{-3}$, for comparison, air density on earth is about $10^{19} \,cm^{-3}$) and the temperature can range from $\sim 10^4\, K$ to $10^7\, K$, therefore it is exceedingly hard to observe in emission as emission flux is directly proportional to the gas density. However, with the advent of groundbreaking space and ground-based telescopes, it can be studied in absorption against a bright background object.

In my PhD thesis, I explored the nature of the complex gas flows in the galaxies' circumgalactic medium (see figure at the top) using absorption lines detected in the spectra of background [Quasars](https://en.wikipedia.org/wiki/Quasar). My goal was to constrain the physical properties of these gas flows with the absorption lines that trace different phases in the CGM. [The setup is the following,](/images/cgm/my_cgm_process.png) when the light emanating from a bright background source (e.g., quasar) passes through the CGM of a foreground galaxy, it can get absorbed and cause absorption dips in the spectrum at redshifts smaller than the quasar redshift.

The different absorption lines can trace [different phases](/images/cgm//absorber_phase.jpg) and physical processes in the CGM and help us understand their connection to galaxy properties and its environment. For e.g., MgII (Mg$^{+}$, it's a doublet line transition with wavelengths 2796 and 2803Å) and FeII (Fe$^{+}$, multiple lines) are tracers of the cold phase ($T \sim 10^4\, K$) of CGM, while CIV (C$^{3+}$, a doublet line transition with wavelengths 1548 and 1550Å) traces the warm-hot ($T \sim 10^5\,K$) CGM. In my thesis, I explored the nature and origin of MgII absorbers in the CGM of star-forming and passive galaxies as well as as in galaxy clusters by characterizing their spatial distribution. Understanding the connection between this gas and the galactic properties and its environment does provide more insights into the physical processes governing galaxy formation and evolution.

Below are some of my work in this field.

**<u>The cool circumgalactic medium of galaxies</u>**

In [(Anand et al. 2021)](https://arxiv.org/abs/2103.15842), I connected MgII absorbers with CGM of [emission-line galaxies (ELGs or star-forming)](https://www.usm.uni-muenchen.de/people/saglia/praktikum/galspectra/node4.html) and [luminous red galaxies (LRGs or passive)](https://classic.sdss.org/dr2/products/general/edr_html/node53.html) from the SDSS DR16 to characterize the properties of cold gas in their CGM. With a very robust statistical analysis, our study implied that cool circumgalactic gas has a different physical origin for star-forming versus quiescent galaxies. We find that both MgII absorption and its covering fraction are 2 - 5 times higher in the CGM of ELGs than LRGs within ~ 50 kpc from the galaxy. Also, there is a very sharp decline in the covering fraction for both kinds of galaxies, and at large distances, they are within the error bars (see left Figure). The rapid decline in the covering fraction at ~ 50 kpc implies that MgII properties are regulated by galactic outflows in the inner part of CGM, while it is tightly linked with the dark matter halo in outer regions.

<p float="center;" style="text-align: center;">
  <img src="/images/mgii_work/mgii_covering_fraction.png" style="width:90%; border:1; display:block”">
  <figcaption>Left: MgII covering fraction in the CGM of star-forming (blue) and passive galaxies (red). Right: MgII covering fraction within galactic halo as a function of star formation rate of galaxies. Both figures are from Anand et al. 2021</figcaption>
</p>

We also find that the stellar activity of ELGs plays a very important role in enriching their CGM, where the MgII covering fraction correlates strongly with the star formation activity (SFR) of the galaxy (see right Figure). In addition, we also see that MgII is rarely detected in the massive halos. The relative line-of-sight (LOS) velocity analysis also supports an outflow origin of MgII gas in ELGs, where the velocity dispersion of the absorbing cloud relative to the halo is similar to the virial velocity of the dark matter halo. On the other hand, it is suppressed by 40-50 % in the LRGs, suggesting a different origin of MgII gas in their halo, possibly accretion or stripping from the neighboring halo. To summarize, our analysis, combined with previous studies, implied that cool circumgalactic gas has a different physical origin for star-forming versus quiescent galaxies.

**<u>The cool metal gas in galaxy clusters</u>**

In [Anand et al. 2022](https://arxiv.org/abs/2201.07811), I extended the MgII absorber study to the galaxy clusters. In this high mass regime (see Figure on left), we have the potential to shed light on the role of the environment in shaping the CGM of galaxies. Cluster halo gas known as the [intracluster medium (ICM)](https://en.wikipedia.org/wiki/Intracluster_medium) is heated up to high temperatures ($T \sim 10^7 - 10^8$ K) due to gravitational collapse. In addition, outflows powered by supermassive black holes in the center of clusters can also heat the gas. The hot ICM emits mostly at X-ray wavelengths due to radiation from thermal [bremsstrahlung](https://en.wikipedia.org/wiki/Bremsstrahlung) produced in the highly ionized gas. Although the ICM is hot, cold/cool gas has sometimes been detected in and around clusters. The most frequently observed elements are hydrogen (Hα, Lyα) and metal absorption lines (MgII, OVI), which are detected in the spectra of background quasars.

The absorber-cluster cross-correlation study using our MgII absorber catalog and galaxy clusters from the legacy survey imaging of [Dark Energy Spectroscopic Instrument (DESI)](https://en.wikipedia.org/wiki/Dark_Energy_Spectroscopic_Instrument) [data release (DR8)](https://www.legacysurvey.org/dr8/description/) is one of the most extensive such studies to date, with $160,000$ MgII absorbers and $72,000$ clusters with spectroscopic redshifts. I characterized the nature and origin of MgII absorbers in galaxy clusters, where most of the [intracluster medium (ICM)](https://en.wikipedia.org/wiki/Intracluster_medium) is mainly filled with hot plasma ($T\sim 10^7$ K).

<p float="left;" style="text-align: center;">
  <img src="/images/cluster_work/mgii_surf_dens.png" style="width:45%; border:1; display:block”">
  <img src="/images/cluster_work/ew_vs_sfr.png" style="width:45%; border:1; display:block”">
  <figcaption>Left: MgII surface density around galaxy clusters. Right: Equivalent width as a function of star formation rate of cluster galaxies. Both figures are from Anand et al. 2021</figcaption>
</p>

Despite the hot ICM, our analysis shows a significant covering fraction ($3-5\%$) of cold gas ($T \sim 10^4$, traced by MgII absorbers) in cluster environments on virial scales. On the other hand, the surface mass density (see Figure on left) of MgII absorbers is $2-3$ times higher in clusters than luminous red galaxies (LRGs). However, the surface mass density is $5-10$ lower than emission-line galaxies (ELGs). While the covering fraction of cool gas in clusters decreases with increasing mass of the central galaxy, the total MgII mass within $r_{500}$ is nonetheless $\sim 10$ times higher than for SDSS LRGs. The MgII covering fraction/surface mass density versus impact parameter is well described by a power law in the inner regions and an exponential function at larger distances. The characteristic scale of the transition between these two regimes is smaller for large [equivalent width](https://en.wikipedia.org/wiki/Equivalent_width) absorbers ($EW > 1Å$), implying different origin of weak and strong absorbers in dense environments.

Furthermore, I also investigated the connection between MgII absorbers and the member galaxies of the cluster. Cross-correlating MgII absorption with photo -z selected cluster member galaxies from DESI reveals a statistically significant connection. The median projected distance between MgII absorbers and the nearest cluster member is $\sim200$ kpc, compared to $\sim 500$ kpc in random mocks with the same galaxy density profiles. We do not find a correlation between MgII strength and the star formation rate of the closest cluster neighbor (See figure on the right). This suggests that cool gas in clusters, as traced by MgII absorption, is (i) associated with satellite galaxies, (ii) dominated by cold gas clouds in the intracluster medium rather than by the interstellar medium of galaxies, and (iii) may originate in part from gas stripped from these cluster satellites in the past.

**<u>Understanding the evolution of metal absorbers in the universe using large cosmological surveys</u>**

Currently, I am also looking into the small and large scale [clustering properties]([https://en.wikipedia.org/wiki/Quasar](https://en.wikipedia.org/wiki/Correlation_function_(astronomy))) of cool and warm (traced by MgII and CIV absorbers in the spectra of [quasar](https://en.wikipedia.org/wiki/Quasar)) in the Universe <span style="color:blue">(Anand+ in prep.)</span>. The scales at which these absorbers show excess clustering against the random background can trace large-scale structures in the universe. Previous studies limited by small sample sizes suffer from large uncertainties on those scales, which can reduced by orders of magnitude with our large sample of absorbers. Since the physical origin of cool and warm gas in the universe is significantly different, those differences would be visible on the clustering amplitudes. I also plan to put constraints on the gas fraction (Omegas) for these metals in our universe at different epochs.

## **<u>Data science methods</u>**

### **<u>Automated pipelines for absorption detection in astronomical spectra</u>**

In [(Anand et al. 2021)](https://arxiv.org/abs/2103.15842), I utilized the largest quasar catalog from the [SDSS Data Release 16 (DR16)](https://www.sdss.org/dr16/) to search for MgII absorbers in their spectra. To achieve this, I developed an automated pipeline that models the quasar continuum and detects Mg II doublets in the spectra. The pipeline is highly parallelized and optimized, enabling the processing of thousands of quasar spectra within minutes.

<p float="center" style="text-align: center;">
  <img src="/images/mgii_work/spec.png" style="width:80%; border:1; display:block”">
  <figcaption>Quasar spectra (black) with NMF continuum (red) and detected MgII absorbers (Anand et al. 2021)</figcaption>
</p>

The pipeline employs a dimensional reduction technique known as [Non-negative matrix factorization (NMF)](https://en.wikipedia.org/wiki/Non-negative_matrix_factorization), which decomposes the quasar intrinsic emission features into eigenvalues and eigenspectra to model the quasar continuum.

Additionally, I developed an automated metal absorber detection pipeline called, [qsoabsfind](https://github.com/abhi0395/qsoabsfind), which utilizes a matched kernel convolution technique combined with adaptive signal-to-noise (S/N) criteria. The pipeline is versatile and can be employed to detect doublet profiles (absorption with two lines) in various spectral datasets (such as SDSS and DESI). It is highly efficient, optimized for parallel processing on hundreds of quasars, and can identify absorbers in thousands of quasar spectra within minutes. Moreover, it can generate simulated mock absorber catalogs for N-dimensional correlation analyses.

Initially, the detection algorithm was applied to the entire quasar dataset from SDSS DR16, resulting in the compilation of the largest available [MgII / FeII catalog](https://wwwmpa.mpa-garching.mpg.de/SDSS/MgII/) available to date, which includes around 160,000 systems. The figure above illustrates a quasar spectrum with normalized flux (black), an NMF continuum fit (red), and detected Mg II absorbers, showcasing the pipeline's capabilities.

### **<u>New methods of galaxy spectral fitting for redshift estimation</u>**

With the advent of ongoing large spectroscopic surveys, analyzing vast numbers of astronomical spectra and accurately measuring their distances has become increasingly important. As we advance toward [precision cosmology](https://www.kavlifoundation.org/news/precision-cosmology), obtaining precise [redshift](https://en.wikipedia.org/wiki/Redshift) measurements of galaxies and quasars is crucial for all major cosmological surveys. Recent surveys, such as DESI, are collecting unprecedented volumes of astronomical spectra to perform next-generation cosmological analyses, making accurate redshift determination one of the key challenges we face.

Given the extensive volume of data, manually inspecting millions of spectra to determine the best redshifts is impractical. Instead, we must rely on dimensional reduction techniques to model the spectra of these objects. One widely used method is [Principal Component Analysis (PCA)](https://en.wikipedia.org/wiki/Principal_component_analysis), which reduces a large set of spectral features into their principal components (orthogonal eigenvectors) and reconstructs spectra using a linear combination of these components. While PCA is computationally efficient and fast, it has notable limitations—it does not consider the physical characteristics of astronomical objects, often leading to unphysical modeling or overfitting of the input spectra.

<p float="center;" style="text-align: center;">
  <img src="/images/archetype_work/algorithm.png" style="width:80%; border:1; display:block”">
  <figcaption>A schematic of our archetype based per camera polynomial fitting (Anand et al. 2024)</figcaption>
</p>


In my recent work [Anand et al. 2024](https://arxiv.org/abs/2405.19288), I developed a computationally efficient galaxy archetype-based redshift estimation and spectral classification method (see figure above) for the Dark Energy Survey Instrument (DESI) survey. Our proposed approach improves upon this existing method by refitting the spectra with carefully generated physical galaxy archetypes combined with additional terms designed to absorb data reduction defects and provide more physical models to the DESI spectra. We test our method on an extensive dataset derived from the survey validation (SV) and Year 1 (Y1) data of DESI. Our findings indicate that the new method delivers better redshift success rates for them while reducing catastrophic redshift failure by 10−30%. At the same time, results from millions of targets from the main survey show that our model has relatively higher redshift success and purity rates (0.5−0.8% higher) for galaxy targets while having similar success for QSOs.

Although this method is slower than the classic PCA, it effectively addresses the issues of unphysical modeling and overfitting. It is also generic and can easily be extended to other upcoming surveys such as [WEAVE](https://www.ing.iac.es/astronomy/instruments/weave/weaveinst.html), [WAVES](https://wavesurvey.org/) and [PFS](https://pfs.ipmu.jp/) on large optical telescopes. The [github repository](https://github.com/desihub/redrock) details the algorithm and code.

## **<u>Past research interests and projects</u>**

During my undergraduate studies, I worked on a few other topics in astronomy. In addition to that, I also explored some topics in high-energy physics and computational nonlinear dynamics. I still like those topics and would love to explore them in the future. You can find more about my past projects [here](/pages/pastprojects).
