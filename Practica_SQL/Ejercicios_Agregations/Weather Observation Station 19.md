# Weather Observation Station 19



Consider P1 (a,c)  and P2 (b,d) to be two points on a 2D plane where (a,b)  are the respective minimum and maximum values of Northern Latitude (LAT_N) and (c,d)  are the respective minimum and maximum values of Western Longitude (LONG_W) in STATION.

Query the Euclidean Distance between points  and  and format your answer to display  decimal digits.

Input Format

The STATION table is described as follows:

[![tabla](https://s3.amazonaws.com/hr-challenge-images/9336/1449345840-5f0a551030-Station.jpg "tabla")](https://www.hackerrank.com/challenges/weather-observation-station-19/problem "tabla")

where LAT_N is the northern latitude and LONG_W is the western longitude.

Solución: 
select round(sqrt((power((min(lat_n)-max(lat_n)),2) + power((min(long_w)-max(long_w)),2))),4) from station ;
