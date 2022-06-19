# Surfs Up
## Overview
##### Wanting to open a Surf n' Shake shop in Oahu, we are pitching our business plan to potential investors. To determine if the weather could detrimentally influence the success of our surf shop, we analyzed past weather data. Instead of establishing an extensive database with a server through PostgreSQL, we utilized SQLite, SQLAlchemy, and Flask to present our findings to investors. 
## Results
##### While it's easy to think that a surf shop could be successful in the summer months of Oahu, we need to know that our shop will be successful year-round. To find how temperatures vary from summer to winter, we wrote queries that would pull several years’ worth of data for the months of June and December, independently. The summary statistics of each of our queries can be seen in the images below (June on the left, December on the right).
![june_temp_summary.PNG](https://github.com/carinaediaz/surfs_up/blob/main/Resources/june_temp_summary.PNG)
![dec_temp_summary.PNG](https://github.com/carinaediaz/surfs_up/blob/main/Resources/dec_temp_summary.PNG)
##### The results show that Oahu's average temperature does not vary much year-round. December's average temperature is 3.9° lower than the average temperature in June. The maximum temperature in June is 2° higher than the maximum in December. We can also note that the standard deviation is low and similar between the two seasons, further solidifying our proposition for a successful surf shop in Oahu year-round with temperatures that vary less than 30° between December's lowest temperature and June's highest. 
## Summary
##### Overall, we have a solid business plan to present to potential investors for our Surf n' Shake shop, as temperatures do not vary much year-round in Oahu. While temperatures may not vary vastly, we should also account for precipitation. Being closer to the equator, Oahu may be more likely to experience more rainfall and rain isn't ideal for surfing. Two additional queries we could write would investigate pulling the precipitation per day for the months of June and December. Examples of those queries and the summary statistics (June on the left, December on the right) they would produce are included below. 
```
june_prcp_results = session.query(Measurement.date, Measurement.prcp).\
  filter(extract('month', Measurement.date) == 6).all()
dec_prcp_results = session.query(Measurement.date, Measurement.prcp).\
  filter(extract('month', Measurement.date) == 12).all()
```
![june_prcp_summary.PNG](https://github.com/carinaediaz/surfs_up/blob/main/Resources/june_prcp_summary.PNG)
![dec_prcp_summary.PNG](https://github.com/carinaediaz/surfs_up/blob/main/Resources/dec_prcp_summary.PNG)
##### These queries show that precipitation is relatively low year-round, but with a slight increase in the average per day in the winter. Additional queries like these could help us secure more support from investors.
