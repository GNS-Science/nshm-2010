# nshm-2010

This repository provides the source model files necessary for running the GNS Science 2010 National Seismic Hazard Model (NSHM) in the <a href="https://www.globalquakemodel.org/oq-get-started">OpenQuake Engine</a>. The NSHM source models for New Zealand provided by GNS Science currently are:
* 2010_NewZealand_NSHM_source_model-1y.xml
* 2010_NewZealand_NSHM_source_model-50y.xml
* 2010_NewZealand_NSHM_source_model-100y.xml

These file are intended to for investigation times of 1 year, 50 years and 100 years respectively, and differ only in conditional probabilities of rupture for a small number of faults. These files are subject to change, please check back regularly for updates.

These files comprise the fifth corrected version of the 2010 New Zealand National Seismic Hazard Model published by Stirling et al. (2012; reference below).

The 2010 New Zealand National Seismic Hazard Model uses the McVerry et al. (2006) GMPE for all tectonic region types: 
* Active Shallow Crust, 
* Volcanic, 
* Subduction Interface, 
* Subduction Intraslab.

More comprehensive, alternative GMPE logic trees are possible in OpenQuake.

The following corrections have been made since the Stirling et al. (2012) publication:
* The background source/distributed seismicity model has been corrected. This was a relatively simple fix regarding application of floor level values. Additionally, the area of the Auckland/Northland distributed seismicity zone has been expanded from that published in Stirling et al. (2012). 
(correction made by M Gerstenberger)

* Four fault sources in the Wellington region have conditional probabilities of rupture. They are OhariuC, OhariuS, WellWHV, and WairarapNich. The occurrence rates differ for the 1-year, 50-year and 100-year models.

* Corrected occurrence rates (1/recurrence interval) for subduction interface sources for the Hikurangi and Fiordland subduction zones. These values were previously only determined by apportioning slip rate by event frequency, which was insufficient. The corrected rates use the single event displacement in addition to slip rate.
  (corrections made by G H McVerry, E R Abbott, T Goded; Jan 2018, Oct 2018, May 2019)

* WaimeaN, WaimeaC, and WaimeaS fault sources now represent the 2010 WaimeaN and WaimeaS sources.
  (corrections made by G H McVerry, R Van Dissen, T Goded; Nov 2018)
  
* The source geometries for PaValley, WhirinakiALL, and HikALL have been revised so that they are compatible with OpenQuake complex source geometry requirements.
  (corrections made by N Litchfield, P Villamor; Nov 2018)

* The Greendale fault source was previously mistakenly left out. It has now been added back into the model.
	(Feb 2019)
    
* Time-dependent occurrence rates for the following fault sources have been corrected following the resolution of an error in the code that produced the values (pers comm. David Rhoades): OhariuC, OhariuS, WellWHV, WairarapNich.
	(Nov 2018)

It should be noted that this fault source model largely preceded the 2010 
Darfield earthquake, so does not include conditional probabilties/time 
dependent recurrence intervals introduced for some Canterbury region faults 
post-Darfield and post-Christchurch, but does include the Greendale fault
source.

**Further reading**

This model forms part of the <a href="https://hazard.openquake.org/gem/models/NZL/">Global Earthquake Model (GEM) Global Mosaic of Hazard Models</a>. 


**References**

McVerry GH, Zhao JX, Abrahamson NA, Somerville PG. 2006. New Zealand 
    acceleration response spectrum attenuation relations for crustal and 
    subduction zone earthquakes. *Bulletin of the New Zealand Society for 
    Earthquake Engineering*. 39(4):1-5.

Stirling MW, McVerry GH, Gerstenberger MC, Litchfield NJ, Van Dissen RJ, 
    Berryman KR, Barnes P, Wallace LM, Villamor P, Langridge, R.M, et al. 2012. 
    National seismic hazard model for New Zealand: 2010 update. *Bulletin of the 
    Seismological Society of America*. 102(4):1514-1542; 
    doi:<a href="https://doi.org/10.1785/0120110170">10.1785/0120110170</a>.
