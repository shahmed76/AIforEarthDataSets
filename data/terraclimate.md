# TerraClimate

## Overview

TerraClimate is a dataset of monthly climate and climatic water balance for global terrestrial surfaces from 1958-2019. These data provide important inputs for ecological and hydrological studies at global scales that require high spatial resolution and time-varying data. All data have monthly temporal resolution and a ~4-km (1/24th degree) spatial resolution. The data cover the period from 1958-2019.

Source: [Climatology Lab](http://www.climatologylab.org), University of California, Merced

Domain: global, 1958-2019

Resolution: 4km, monthly

Documentation and a complete description of the TerraClimate dataset are available on the [TerraClimate home page](http://www.climatologylab.org/terraclimate.html).

This dataset was curated and brought to Azure by [CarbonPlan](https://carbonplan.org/).

## Storage resources

Data are stored in blobs in the West Europe Azure region, in the following folder:

`https://cpdataeuwest.blob.core.windows.net/cpdata/raw/terraclimate/4000m/raster.zarr`

Data are stored in [Zarr](https://zarr.readthedocs.io/en/stable/) format, indexed by latitude, longitude, and time.  The following variables are available:

* `aet` (actual evapotransporation)
* `def` (climatic water deficit)
* `pdsi` (Palmer Drought Severity Index)
* `pet` (reference evapotransporation)
* `ppt` (acculumated precipitation)
* `ppt_station_influence` (number of stations used for ppt)
* `q` (runoff)
* `soil` (soil moisture at end of month)
* `srad` (downward shortwave radiance flux at the surface)
* `swe` (snow water equivalent at end of month)
* `tmax` (maximum 2m temperature)
* `tmax_station_influence` (number of stations used for tmax)
* `tmin` (minimum 2m temperature)
* `tmin_station_influence` (number of stations used for tmin)
* `vap` (2m vapor pressure)
* `vap_station_influence` (number of stations used for vap)
* `vpd` (vapor pressure deficit)
* `ws` (10m wind speed)

We also provide a read-only SAS (<a href="https://docs.microsoft.com/en-us/azure/storage/common/storage-sas-overview">shared access signature</a>) token to allow access to this data via, e.g., BlobFuse, which allows you to mount blob containers as drives:

`?sv=2019-12-12&si=cpdata-ro&sr=c&sig=tqRGrmdYYa9WYkaPi0wWOD0nalRdNGTZNe97GL2enDA%3D`

Mounting instructions for Linux are [here](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-how-to-mount-container-linux).

Large-scale processing is best performed in the West Europe Azure data center, where the data are stored.  If you are using this data for environmental science applications, consider applying for an [AI for Earth grant](http://aka.ms/ai4egrants) to support your compute requirements.


## Sample code

A complete Python example of accessing and plotting TerraClimate data is available in the accompanying [sample notebook](https://nbviewer.jupyter.org/github/microsoft/AIforEarthDataSets/blob/main/data/terraclimate.ipynb).


## Citation

If you use this data in a publication, please cite:

Abatzoglou JT, Dobrowski SZ, Parks SA, Hegewisch KC. TerraClimate, a high-resolution global dataset of monthly climate and climatic water balance from 1958–2015. Scientific data. 2018 Jan 9;5(1):1-2.


## Contact

For questions about this dataset, contact [`aiforearthdatasets@microsoft.com`](mailto:aiforearthdatasets@microsoft.com?subject=terraclimate%20question).


## Notices

Microsoft provides this dataset on an "as is" basis.  Microsoft makes no warranties (express or implied), guarantees, or conditions with respect to your use of the dataset.  To the extent permitted under your local law, Microsoft disclaims all liability for any damages or losses - including direct, consequential, special, indirect, incidental, or punitive - resulting from your use of this dataset.  This dataset is provided under the original terms that Microsoft received source data.

