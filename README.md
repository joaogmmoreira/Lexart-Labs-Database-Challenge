# Lexart-Labs-Database-Challenge
João Moreira Database challenge - Support Engineer

Query For getting to desired result:

CREATE TABLE AverageLifeExpectancy
SELECT 
(FLOOR(AVG(country.LifeExpectancy))) AS LifeProm,
country.Continent AS Region
FROM world.country
WHERE continent IN ('South America', 'North America', 'Asia')
AND country.LifeExpectancy IS NOT Null
GROUP BY continent
ORDER BY Region DESC;
