# (Dataset Exploration Flights)
## by Joris Axel DA MATHA


## Dataset


> This dataset fond on [Source](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/HG7NV7) explores reporting flights in US including carriers, arrival and depature delays and reasons for delays, from 1987 to 2008. Including a lot of variables as mentionned in following table: 

| **`Columns`**        | **`Description`**  |  
| ------------- |-------------:|
| `Year`| 2004-2008 |
| `Month` |1-12 (January to December)    |
| `DayofMonth`| 1-31   |
| `DayofWeek`   |1-7 (Monday to Sunday)  |
| DepTime      | Actual departure time (local, hhm m)  |
| CRSDepTime |Scheduled departure time (local, hhmm)    |
| ArrTime   |Actual arrival time (local, hhmm)  |
| CRSArrTime      | Scheduled arrival time (local, hhmm)  |
| UniqueCarrier | Unique carrier code     |
| FlightNum   |  Flight number  |
| TailNum      | Plane tail number  |
| ActualElapsedTime | Actual Elapsed Time in minutes     |
| CRSElapsedTime | CRS Elapsed Time in minutes     |
| AirTime | Air Time in minutes     |
| `ArrDelay` | Arrival delay in minutes     |
| `DepDelay` | Departure delay in minutes  |
| `Origin` | Origin IATA airport code     |
| `Dest` | Destination IATA airport code     |
| `Distance` | Distance in miles     |
| TaxiIn | Taxi in time in minutes     |
| TaxiOut | Taxi out time in minutes     |
| `Cancelled` | Indicates if the flight was cancelled     |
| `CancellationCode` | Reason for cancellation (A = carrier, B = weather, C = NAS, D = security)     |
| `Diverted` | 1 = yes, 0 = no     |
| `CarrierDelay` | Carrier Delay Time in minutes     |
| `WeatherDelay` | Weather Delay Time in minutes     |
| `NASDelay` | NAS Delay Time in minutes     |
| `SecurityDelay` | Security Delay Time in minutes     |
| `LateAircraftDelay`|Late Aircraft Delay in minutes   |



## Summary of Findings

> We are facing a very large set of data , about 1Md rows. Due to some limited ressources for reading i focused my exploration on the last 4 years contents (2004-2008), so on more than 24M flights. 

I sought to answer three main questions: 
- Are there certain destination or arrival cities that experience more delays or cancellations? 
- What are the main factors behind the cancellation of flights? 
- What are the preferred times for flights to occur? Are there changes over several years?

I start firstly with a global view in arrival and departure delays in dataset. As first insight, i discovered that we have negative delays, means some flights land in advance or arrived in advance. To avoid any misunderstanding in my next analysis i focused the further investigations on flights with non negative departure delays. Even after that we have certain flights arrived at destination in advance but the time gain was very negligible. Then i searched most popular cities/countries subjected to delay at departure and arrival to continue investigations about the flights delayed distribution per year, months and days week. I saw that the amount of flights in dataset are more between 2005 and 2007. We have few flights in 2008 by refering to data shape of these years. Based on 10 most common destinations,the majority of flights are made in March and very few flights on september. Most flights delayed are scheduled for Friday and Thursday and less on saturdays. My last univariate exploration were about the amount of cancelled flights in data.There were very few inside and most of flights which are delayed due to Carrier, and after weather, very few delayed by Security. 

After these global insights, i attacked the first and second question, i discovered that among the cancellation and delay factors (Carrier, NAS, Wheather and Security ) the Carrier and NAS could more issue the cancellation of flights. But about delay factors, i discovered that mainly the late aircraft delay can highly the flight departure and in parallel the NAS delay affects a lot the delay at arrival. 

Finally i tried to figure out the preferred times for flights. Based on the 10 most popular cities, i saw that the may and september months flights are less subjected to delay. But a last big discover there were some countries always subjected to delay at arrival (ORD and EWR for example).

## Key Insights for Presentation

> Firstly we will have a global view of all delayed flights and how they are distributed in dataset. After, we will have more visibility about cancelled flights in dataset. Then we will apreciate the real impact of great factors delays followed by cancellation factors impact according to city and time. Finally we will have a final overview of flights delay per month on 10 most frequent destinations and departure cities. 
