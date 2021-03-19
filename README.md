# Patterns in the useo of Taxis in Chicago



| Project Description | Libraries Used | Source of Data |
| :---------------------- | :---------------------- | :---------------------- | 
| I am working as an analyst at Zuber; a new ride-sharing company that's launching in Chicago. My task is to find patterns in the available information. I want to understand passenger preferences and the impact of external factors on rides, i.e. I will study a database, analyze data from competitors, and test a hypothesis about the impact of weather on ride frequency. | *pandas*, *matplotlib.pyplot*, *numpy*, *seaborn*, *scipy*, *requests*, *BeautifulSoup* | Practicum by Yandex |
 
 
 ## Description of Data
 
A database with info on taxi rides in Chicago:

### Neighborhoods table: data on city neighborhoods
- `name:` name of the neighborhood
- `neighborhood_id:` neighborhood code

### Cabs table: data on taxis
- `cab_id:` vehicle code
- `vehicle_id:` the vehicle's technical ID
- `company_name:` the company that owns the vehicle

### Trips table: data on rides
- `trip_id:` ride code
- `cab_id:` code of the vehicle operating the ride
- `start_ts:` date and time of the beginning of the ride (time rounded to the hour)
- `end_ts:` date and time of the end of the ride (time rounded to the hour)
- `duration_seconds:` ride duration in seconds
- `distance_miles:` ride distance in miles
- `pickup_location_id:` pickup neighborhood code
- `dropoff_location_id:` dropoff neighborhood code

### Weather records table: data on weather
- `record_id:` weather record code
- `ts:` record date and time (time rounded to the hour)
- `temperature:` temperature when the record was taken
- `description:` brief description of weather conditions, e.g. "light rain" or "scattered clouds" (an SQL CASE was created to categorize desciption into `Good`and `Bad`)
