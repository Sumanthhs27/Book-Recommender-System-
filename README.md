# WhichBook 

### <a href=https://book-recommender-system-27.herokuapp.com/>Check out the Deployed Model here</a>

Recommendation Systems are one of the largest application areas of Machine Learning. They enable tailoring personalized content for users, thereby generating revenue for businesses

There are 4 main types of recommendation systems:

### 1. Popularity based Filtering:

### 2. Content based Filtering:
Recommendations are based on user's past likes/ dislikes & item feature space. The system makes recommendations which are similar to items the user has liked in the past. Items are considered similar based on item's features such as author, publisher, genre etc

### 3. Collaborative Filtering:
Recommendations are based solely on user's past likes/ dislikes & how other users have rated other items. The system does not take into consideration an item's features like author, publisher, genre etc nor a user's features like age, gender, location etc. These take either a memory based approach or a model based approach

### 4. Hybrid Filtering:

## -------------------------------------------------------------------------------------

## Project Description:
<p>WhichBook is a Collaborative Filtering and Popularity based Book Recommendation System which recommends the users a selection of books based on their interests.</p>

## Data Set:
<p>Data used for this project was taken from <a href=https://www.kaggle.com/datasets/arashnic/book-recommendation-dataset/>Kaggle</a>. </p> 

### 1. Data Cleaning and Pre-Processing: 
The dataset consists of three tables; Books, Users, and Ratings. Data from all three tables are cleaned and preprocessed separately as defined below briefly:<br><br>
For Books Table:
* Drop all three Image URL features.
* Check for the number of null values in each column. There comes only 3 null values in the table. Replace these three empty cells with ‘Other’.
* Check for the unique years of publications. Two values in the year column are publishers. Also, for three tuples name of the author of the book was merged with the title of the book. Manually set the values for these three above obtained tuples for each of their features using the ISBN of the book.
* Convert the type of the years of publications feature to the integer.
* By keeping the range of valid years as less than 2022 and not 0, replace all invalid years with the mode of the publications that is 2002.
* Upper-casing all the alphabets present in the ISBN column and removal of duplicate rows from the table.

For Users Table:
* Check for null values in the table. The Age column has more than 1 lakh null values.
* Check for unique values present in the Age column. There are many invalid ages present like 0 or 244.
* By keeping the valid age range of readers as 10 to 80 replace null values and invalid ages in the Age column with the mean of valid ages.
* The location column has 3 values city, state, and country. These are split into 3 different columns named; City, State, and Country respectively. In the case of null value, ‘other’ has been assigned as the entity value.
* Removal of duplicate entries from the table.

For Ratings Table:
* Check for null values in the table.
* Check for Rating column and User-ID column to be an integer.
* Removal of punctuation from ISBN column values and if that resulting ISBN is available in the book dataset only then considering else drop that entity.
* Upper-casing all the alphabets present in the ISBN column.
* Removal of duplicate entries from the table.

## -------------------------------------------------------------------------------------

### 2. Algorithms Implemented:
#### 2.1 Popularity Based Recommendation :

* ##### Popular in the Whole Collection <br>
We have sorted the dataset according to the total ratings each of the books have received in non-increasing order and then recommended top 50 books.

#### 2.2 Collabaorative Filtering Based Recommendation :
* ##### Collaborative Filtering Recommendation System works by considering user ratings and finds cosine similarities in ratings by several users to recommend books. To implement this, we took only those books' data that have at least 200 ratings in all.


### 3. Libraries Used:

* ipython-notebook - Python Text Editor
* sklearn - Machine learning library
* seaborn, matplotlib - Visualization libraries
* numpy, scipy- number python library
* pandas - data handling library



























