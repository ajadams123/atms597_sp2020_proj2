# atms597_sp2020_proj2

Project 2 for Alex Adams, Jeff Thayer, Lina Rivelli-Zea

This python module reads in minimum and maximum daily temperatures for Berlin, Germany from 1876-2019 that were retrieved from the NCEI Global Historical Climatology Network - Daily (GHCND) dataset and plots climate stripes using normalized anomalies following the approach of Ed Hawkins at the University of Reading (https://showyourstripes.info/). 

After reading in the daily temperature extremes from a '.csv' file using pandas and pivoting the temperature extrema into separate columns, they are converted to daily-averaged temperatures using (TMAX + TMIN)/2. These daily-averaged temperatures are then grouped by year, month, and week before being averaged again. This results in yearly-averaged, monthly-averaged, and weekly-averaged daily-averaged temperatures. 

Following the climate stripping methodology of Ed Hawkins, our baseline time period average from which to compare the dataset is the mean daily-averaged temperature for 1971-2000. This value is subtracted from the yearly-averaged, monthly-averaged, and weekly-averaged daily-averaged temperatures to create anomalies. To better account for variance in the temperature dataset, these anomalies are then normalized by the standard deviation over each respective averaging period using the longer period 1901-2000. This results in yearly-averaged, monthly-averaged, and weekly-averaged daily-averaged normalized temperature anomalies relative to 1971-2000 and normalized by 1901-2000.
