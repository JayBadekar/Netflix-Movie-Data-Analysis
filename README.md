Netflix Movie Data Analysis :-

An exploratory data analysis (EDA) project in Python that cleans and reshapes a movie dataset of 9,827 titles to uncover patterns in genres, ratings, popularity and release years.

Objectives :-

Answer five questions about the catalogue :-

What is the most frequent genre?
Which rating class (Popular, Average, Below average, Not popular) is largest?
Which movie has the highest popularity, and what are its genres?
Which movie has the lowest popularity, and what are its genres?
How are releases distributed across years?
Dataset

mymoviedb.csv: 9,827 rows and 9 columns (Release_Date, Title, Overview, Popularity, Vote_Count, Vote_Average, Original_Language, Genre, Poster_Url). The data has no missing values or duplicates.


Data Preprocessing :-

Converted Release_Date to datetime and kept only the year
Dropped Overview, Original_Language and Poster_Url
Grouped Vote_Average into four classes using quartile cutoffs
Dropped the 100 rows that fell outside the rating bins (9,727 movies remained)
Split the comma-separated Genre column so each row holds one genre (25,552 rows, 19 genres)


Key Findings :-

Drama is the most frequent genre: 3,715 entries (14.5% of all genre entries).
Average is the largest rating class (6,613 rows), and 25.5% of rows are rated Popular.
Spider-Man: No Way Home is the most popular movie (popularity 5,083.95), roughly 240 times the median.
The United States vs. Billie Holiday and Threads have the lowest popularity (13.354).
Movie releases rise sharply in recent decades.


Tech Stack :-
Python, pandas, NumPy, Matplotlib, Seaborn


How to Run :-

bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
pip install numpy pandas matplotlib seaborn jupyter
jupyter notebook Netflix_Movie_Data_Analysis.ipynb

Make sure mymoviedb.csv is in the same folder as the notebook.



Limitations :-

Genre counts are tag counts, so movies with several genres are counted more than once.
Rating classes are quartile-based, so they are roughly equal in size by design.



Presentation :-

A slide deck summarising the project is included: Netflix_Movie_Data_Analysis.pptx.
Suggested topics/tags: data-analysis eda python pandas seaborn matplotlib movies netflix data-visualization
