# Surfs_Up

## Overview of Analysis

The purpose for this analysis was to find the temperatures for the months of June and December and summarize the statistics using a combination of the pandas and SQLAlchemy library in Python. The queries to find this information is located in the [SurfsUp_Challenge](https://github.com/stwpf01/Surfs_Up/blob/main/SurfsUp_Challenge.ipynb) file. Results and examples will be explained below.


## Results

### Images

![June](https://github.com/stwpf01/Surfs_Up/blob/main/Resources/June.png)


![December](https://github.com/stwpf01/Surfs_Up/blob/main/Resources/December.png)

### Points and Code Example

- The temperatures for June and December were fairly comparable. Not an extreme difference. 
- December is, unsurprisingly, colder than June, but even December's coldest day is close to June's coldest.   
- The mean temperature for both months is an ideal temperature for most people, therefore the entire span of the months is viable for business.

To filter through the data to only gather the temperatures for these months, the following code was written:

`june = session.query(Measurement.tobs).filter(extract("month", Measurement.date) == 6).all()`

A variable (`june` and/or `dec`) was created to equal a query in the Measurement table for the observed temperature (`tobs`) column. This was then filtered and extracted using the `.filter()` and `extract()` functions, where the month of the data column in the Measurement table equaled 6 or 12 for June and December, respectively.  

## Summary

There does not seem to be any issues in keeping a business open all year long that is contingent upon the weather given the minor difference in temperatures for the months of June and December. Further suggestions would be to determine the average rainfall and average wind speed during those months. While not necessarily deterents given the nature of the business, it would help to know if the rainfall and wind speeds would be too extreme for more casual practitioners of surfing so that the target audience would have to be altered.