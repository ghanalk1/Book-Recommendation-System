# **Book Recommendation System**
## *Problem Statement*
### In a very general way, recommender systems are algorithms aimed at suggesting relevant items to users (items being movies to watch, text to read, products to buy, or anything else depending on industries).
### Recommender systems are really critical in some industries as they can generate a huge amount of income when they are efficient or also be a way to stand out significantly from competitors. The main objective is to create a book recommendation system for users.
### This Book-crossing dataset contains three files: Users, Books, Ratings.
![2324](https://user-images.githubusercontent.com/65157529/182559779-75310450-f01e-4da8-a564-f4d75b6488c5.jpeg)


## *Data Description*
### In some industries, the use of recommender systems is crucial because, when done well, they can be extremely profitable and set themselves apart from their competitors. The main objective of this project  is to create a book recommendation system for users based on different approaches.
### Here, we've used the Book-Crossing dataset, which consists of 3 files. They are:
### Users
> * User-ID: A unique identification number for each user
> * Location:It contains city,state and country  to which the user belongs ,separated by commas
> * Age:The age of the user
### Books
> * ISBN:International Standard Book Number unique to each edition of the book
> * Book-Title:Title of the book
> * Book-Author:Author of the book(incase of several authors only the first is provided)
> * Year-of-Publication:The year in which the particular edition of the book was published
> * Publisher:Name of the Book Publishing company
> * Image-URL-S: URL link to a small version of the book cover displayed on the Amazon website
> * Image-URL-M:	URL link to Medium version image of the book cover displayed on the Amazon website
> * Image-URL-L: URL link to Large sized image of the book cover displayed on the Amazon website
### Ratings
> * User-ID:as mentioned above
> * ISBN:as mentioned above
> * Book-Rating: The rating given by the user (identified by User-ID) for the book (identified by ISBN). It is either explicit,expressed on a scale from 1-10 (higher values denoting higher appreciation), or implicit,expressed by 0.


## *Steps Involved*
### 1. Data Preprocessing
### Books
> * Removed the columns Image-URL-S, Image-URL-M and Image-URL-L which do not provide any information for analysis.
> * The entries in the columns : Book-Title, Book-Author, Year-Of-Publication, and Publisher that were entered incorrectly were fixed, and those entries were replaced with the correct values found through an internet search.
> * Imputed invalid entries in the column Year of Publication with median.
> * Converted ISBN  and Book-Author to uppercase.
> * Duplicates removal.
### Users
> * The null values and the invalid Age column entries were imputed with values from a normal distribution whose mean and standard deviation matched those of the valid Age column entries.
> * In order to better understand the age distribution of users and their book preferences, a new column called ‘Age_group’ was created to categorize users as either children, teens, youth, middle-aged adults, or elderly.
> * Extracted the country name from the ‘Location’ column and corrected the misspelled country names.
> * Checked for duplicates
> * Converted country to uppercase.
### Ratings
> * Converted ISBN to uppercase.
> * Checked for missing values and duplicates
> * Created two distinct dataframes for the entries with implicit ratings (Book-Rating=0) and explicit ratings (Book-Rating!=0).

### 2. EDA
### Here are the key findings:
> * 8 is the most popular rating given by users.
> * The Lovely Bones is the most popular book.
> * Stephen King is the most popular Author.
> * Users between age 30-40 are most active.
> * The country with the most users who have rated the books is the USA.
> * Publisher with most no. of published books: Ballantine Books.

### 3. Collaborative Filtering based Recommender Systems
### The Collaborative Filtering approach first investigates the user’s behaviors, interests, and searches for similar users. It recommends items to users based on the ratings of similar users on various items and by predicting the missing ratings of the items . CF is broadly classified as memory-based and model-based CF.
> * Used KNN algorithm for memory based CF.
> * Implemented Matrix Factorization (SVD) for model based CF.









