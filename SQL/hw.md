

# Problem 1

```sql
SELECT apts.description, AVG(flts.arrive_delay) AS avg_delay
FROM hw6.flights AS flts
LEFT JOIN hw6.airports AS apts ON flts.origin_airport_id = apts.airport_id
GROUP BY apts.description
HAVING COUNT(*) > 100
ORDER BY avg_delay DESC LIMIT 1
;
```
