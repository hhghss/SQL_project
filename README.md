# SQL_project
## This has a dataset of cinema halls in KSA with ratings and comments.


1- 
```
SELECT * FROM project.cleaned_file;
```
![image](https://github.com/user-attachments/assets/d22c6767-e251-46e2-9c58-114c4b896b44)

-----
2- Retrieve the names and ratings of cinema halls with a perfect rating of 5:
```
SELECT name, rating
FROM project.cleaned_file 
WHERE rating = 5;
```
<img src="https://github.com/user-attachments/assets/c4d23643-559d-4819-904e-5bb6757ea0b5" alt="Value Counts Output" width="400"/>

-----
3- Find the top 10 cinema halls with the highest number of reviews:
```
SELECT name, review_count 
FROM project.cleaned_file 
ORDER BY review_count DESC 
LIMIT 10;
```
<img src="https://github.com/user-attachments/assets/bf350f80-80cc-46d5-af7f-34dbcb123f28" alt="Value Counts Output" width="400"/>

-----
4- Retrieve the names and best comments of cinema halls where the comment mentions "comfortable":
```
SELECT name, best_comment 
FROM project.cleaned_file 
WHERE best_comment 
LIKE '%comfortable%';
```
![image](https://github.com/user-attachments/assets/8e80c1c8-4296-4407-97e0-3fc6f8a326e2)

-----
5- Get the names and ratings of cinema halls located in Riyadh:
```
SELECT name, rating 
FROM project.cleaned_file 
WHERE location LIKE '%Riyadh%';
```
<img src="https://github.com/user-attachments/assets/38308203-faba-4bda-be07-1b6492db2353" alt="Value Counts Output" width="400"/>

-----
6- Calculates the average rating for each genre of theaters:
```
SELECT genre, AVG(rating)
FROM cleaned_file
GROUP BY genre;
```
<img src="https://github.com/user-attachments/assets/24f22626-eb14-42be-8beb-8ff033c06626" alt="Value Counts Output" width="400"/>

-----
7- Retrieves unique theater names from the dataset:
```
SELECT DISTINCT name
FROM cleaned_file;
```
<img src="https://github.com/user-attachments/assets/fe354af6-bd3e-4a19-a1ef-81bbec8f83b3" alt="Value Counts Output" width="400"/>

-----
8- Get the names and locations of theaters with a rating of 4 or higher:
```
SELECT name, location 
FROM project.cleaned_file 
WHERE rating >= 4;
```
<img src="https://github.com/user-attachments/assets/f022ee07-ac0e-416d-9562-4167bdd0f256" alt="Value Counts Output" width="400"/>

-----
9- Count the total number of reviews across all theaters:
```
SELECT SUM(review_count) AS total_reviews 
FROM project.cleaned_file;
```
![image](https://github.com/user-attachments/assets/780a2f59-cbf3-4b26-8d2e-4e2183b4510c)

-----
10- List theaters with the best comments that contain more than 50 characters:
```
SELECT name, best_comment 
FROM project.cleaned_file 
WHERE LENGTH(best_comment) > 50;
```
<img src="https://github.com/user-attachments/assets/40567837-5094-415d-8687-668314ff7c55" alt="Value Counts Output" width="400"/>















