# Jack-Duncan-Data-Portfolio

Select * from NBA.players
Select * from NBA.playerstatistics

1)	What school has the highest average draft pick over the past 30 years?

Background checking intial; 

SELECT * 
FROM NBA.players 
WHERE draftRound = 1 and draftNumber between 1 and 25 and draftYear between 1990 and 2020

   
SELECT lastAttended,
       AVG(draftNumber) AS avg_pick
FROM NBA.players
WHERE draftYear between 1990 and 2020
GROUP BY lastAttended
HAVING COUNT(*) >= 10
ORDER BY avg_pick ASC
Limit 1


2)	What is the average weight for point guards in the NBA?

Select *
FROM NBA.playerstatistics
Where lastName = 'Curry' 


SELECT 
    AVG(bodyWeight) AS average_pg_weight
FROM NBA.players
WHERE Guard = 'True'









