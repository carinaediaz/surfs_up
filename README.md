# Surfs Up
## Overview
## Results
![june_temp_summary.PNG](https://github.com/carinaediaz/surfs_up/blob/main/Resources/june_temp_summary.PNG)
![dec_temp_summary.PNG](https://github.com/carinaediaz/surfs_up/blob/main/Resources/dec_temp_summary.PNG)
## Summary
```
june_prcp_results = session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 6).all()
dec_prcp_results = session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 12).all()
```
![june_prcp_summary.PNG](https://github.com/carinaediaz/surfs_up/blob/main/Resources/june_prcp_summary.PNG)
![dec_prcp_summary.PNG](https://github.com/carinaediaz/surfs_up/blob/main/Resources/dec_prcp_summary.PNG)
