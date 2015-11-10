# American Red Cross Smoke Alarm Project

### Big picture
Help Red Cross Home Fire Preparedness Campaign target areas for smoke alarm installs.  Check out the repo [wiki](https://github.com/brooksandrew/arc_smoke_alarm/wiki) for more background information.

### Modeling ideas (working doc)
* https://docs.google.com/document/d/1oJN-QwLVqFHOvrRNtW2KEAkNZ-PuFiqTwa8y3iXx1Sg

### Structure of repo

##### 1. `/models` 
Contains exploration and modeling code to produce risk scores for census tracts.  Each model or indicator has it's own folder.  The suffix of each folder name (_1a, _1c, _3a, etc) correspond to the naming convention in this [model scoping working doc]... which is subject to change.   Each folder should have the code necessary to generate the predictions/risk scores and a .csv of the risk scores themselves for each census tract.  Most model input data is too large to store on Github.  It lives on Google Drive or should be pointed to with a README.md if it's publicly available on the web.  This repo is meant to allow for data science tinkering.  The data for the visualization is pulled from here, aggregated and stored in `aggregate_risk/data/risk_tract.R`

`aggregate_risk/aggregate_models.R` pulls the .csv output from each individual model folder and creates an aggregated risk score at the census tract level which will be used in the [viz repo].

**Note:** the structure of this repo was simply initalized as it is now.  Improvements and structural enhancements/shifts as the project progresses are welcomed!

**Note:** Results from these models will be visualized in the [visualization repo](https://github.com/home-fire-risk/smoke_alarm_map)

[model scoping working doc]: https://docs.google.com/document/d/1oJN-QwLVqFHOvrRNtW2KEAkNZ-PuFiqTwa8y3iXx1Sg/edit
[viz repo]: https://github.com/home-fire-risk/smoke_alarm_map


