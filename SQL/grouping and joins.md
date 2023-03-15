# Working with Bureau of Transportation Statistics Dataset of Flights

### Structure pictured below:

![Flight Dataset DrawSQL](./images/flight_drawsql.png)

#### Query to obtain the airport with the greatest average delay in arriving flights (minimum 100 ariving flights)

```sql
SELECT apts.description, AVG(flts.arrive_delay) AS avg_delay
FROM hw6.flights AS flts
LEFT JOIN hw6.airports AS apts ON flts.origin_airport_id = apts.airport_id
GROUP BY apts.description
HAVING COUNT(*) > 100
ORDER BY avg_delay DESC LIMIT 1
;
```
