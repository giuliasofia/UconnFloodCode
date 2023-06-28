# UconnFloodCode
## These codes were produced as part of the NASA High Mountain Asia program (grant #80NSSC20K1300)
## 28june2023: this is a beta version of the codes ##

This script include the codes to produce a proxy of flood mapping from global available datasets. 

The scripts produce maps of Flood Geomorphic Potential (FGP), calculated as the logarithm of the ratio between the bankfull elevations (estimated using a hydraulic scaling function -HSF-) in the element of the river network closest to the point under examination and the elevation difference between these two points. 
This index was originally defined by ​Samela et al., (2017)​. These scripts provide a modified version of their approach.
For the definition of the HSF, the system infers bankfull widths from the topography, and calculate the bankful elevation from there. For this, bankfull widths are automatically identified according to the methods by ​Sofia, et al., (2017); Sofia et al., (2015)​. The advantage of its implementation is that FGP is automated and does not require any additional information other than terrain data.  

## Important notes:
- The scripts heavily rely on TopoToolbox, provided by Schwanghart and Scherler  
https://github.com/wschwanghart/topotoolbox
- The script downloads the terrain data using the function "readopentopo" included in topotoolbox. The function uses opentopography’s RESTful Web service for global raster data access for seamless download of global digital elevation models. As of  January 1st, 2022, an API authorization key is required for this API. Users can request an API key via myOpenTopo in the OpenTopography portal (https://opentopography.org/developers).
 
## References:
- ​Samela, C., Troy, T. J., & Manfreda, S. (2017). Geomorphic classifiers for flood-prone areas delineation for data-scarce environments. Advances in Water Resources, 102, 13–28. https://doi.org/10.1016/j.advwatres.2017.01.007 
- Schwanghart, W., Scherler, D. (2014): TopoToolbox 2 – MATLAB-based software for topographic analysis and modeling in Earth surface sciences. Earth Surface Dynamics, 2, 1-7. DOI: 10.5194/esurf-2-1-2014
​- Sofia, G., di Stefano, C., Ferro, V., & Tarolli, P. (2017). Morphological Similarity of Channels: From Linear Erosional Features (Rill, Gully) to Alpine Rivers. Land Degradation & Development, 28(5), 1717–1728. https://doi.org/10.1002/ldr.2703 
​- Sofia, G., Tarolli, P., Cazorzi, F., & Dalla Fontana, G. (2015). Downstream hydraulic geometry relationships: Gathering reference reach-scale width values from LiDAR. Geomorphology, 250, 236–248. https://doi.org/10.1016/j.geomorph.2015.09.002 
