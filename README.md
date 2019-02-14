# MITgcm-Offline-HYCOM-Scripts
## Description
The purpose of these scripts it to setup MITgcm to run with the offline package using HYCOM-derived forcing fields (u, v, T & S). These scripts will prepare the offline forcings, the BC, the IC, and the domain/grid files for MITgcm.



## Domain Construction Notes

### Initial Preparation
* Download native HYCOM files from the server at NRL. <X.tar.gz>
* Setup script `transport_calc.csh`
 * Set directories and naming convention to read in grid + bathymetry files
 * Set input and output directories
 * Loop over year/days
 * Run `archv2strmf` for each file
 * For that function you provide
  * idm/jdm - The total grid size
  * The location of the domain cut you want to start at
  * The size of the cut out that you want
  * The depths of the z-layers that you want
* Script writes resulting cut of u and v transports to a netcdf file
 * File includes Lat, Lon, Depth and Time as dimensions


## About us
These codes were developed by _Taylor Shropshire_ at Florida State University as part of the Zooplankton Ecology and Biogeochemistry group [link](http://myweb.fsu.edu/mstukel/).
