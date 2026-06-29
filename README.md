# CC-SQL

```sql
UPDATE supplier
SET name = 'Global Auto Parts Unlimited'
WHERE name = 'United Motor Supply';
```

```sql
SELECT lastname, firstname
FROM customer
WHERE zipcode IN ('75000', '34000')
  AND birth_date IS NOT NULL;
```

```sql
SELECT
    v.vin,
    COUNT(vp.vehicle_part_id) AS vehicle_part_count
FROM vehicle v
INNER JOIN vehicle_part vp
    ON v.vehicle_id = vp.vehicle_id
GROUP BY v.vin;
```

```sql
SELECT
    first_name,
    last_name,
    ROUND(games_played * ppg) AS total
FROM basketball_player_stats
WHERE ROUND(games_played * ppg) >= 1600
ORDER BY last_name ASC;
```
