# Lexart-Labs-Database-Challenge
João Moreira Database challenge - Support Engineer

Query For getting to desired result:<br>

USE world;<br>
CREATE TABLE AverageLifeExpectancy<br>
SELECT<br>
(FLOOR(AVG(COALESCE(country.LifeExpectancy, 0)))) AS LifeProm,<br>
country.Continent AS Region<br>
FROM world.country<br>
WHERE continent IN ('South America', 'North America', 'Asia')<br>
AND country.LifeExpectancy IS NOT Null<br>
GROUP BY continent
ORDER BY Region DESC;<br>
