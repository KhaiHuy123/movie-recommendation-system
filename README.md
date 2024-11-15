# Movie-Recommendation-System 

Here, I've developed a movie search engine utilizing the public "ml-25m" dataset. You can download the dataset [here](https://grouplens.org/datasets/movielens/)

This project was created with the intention of study and research purposes, aiming to build a basic foundation for further exploration. The concept of this project is built upon the limitations of traditional Machine Learning reasoning. Nowadays, a multitude of deep learning models are employed to construct recommendation systems.

One thing must be concerned about is the quality of dataset used . According to announcements from "unforeseen authors" who provide "ml-25m" dataset. There is nothing guaranteed for the correctness of those datasets used in this project .

*Data collection is often seen as a one-time event and is neglected in favour of building better model architecture. As a result, hundreds of hours are lost in fine-tuning models based on imperfect data. According to [Adrew Ng](https://en.wikipedia.org/wiki/Andrew_Ng) , we “need to move from a model-centric approach to a data-centric approach.”* . You can explore more informations [here](https://analyticsindiamag.com/why-andrew-ng-favours-data-centric-systems-over-model-centric-systems/)

The topics *"data approaching and model approching , which one is better ?"*, *"What is the right data ?"* . It make me think too ...

# About Project 

The algorithm employed in this project is based on :
[IDF (inverse document frequency)](https://www.capitalone.com/tech/machine-learning/understanding-tf-idf/) 
, a technique used in text analysis and information retrieval .

How the search engine work ? 

- Step 1 :        

All movie titles, including the input title and titles within the dataset, are transformed into numerical representations. Thankfully, we have support of [sklearn.feature_extraction.text.TFIDFVetorizer](https://scikit-learn.org/stable/modules/generated/sklearn.feature_extraction.text.TfidfVectorizer.html) to perform this task .
        
- Step 2 :

Calculate [consine similarity](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.pairwise.cosine_similarity.html) and compare input title to all titles in dataset. Finally show list of results that have high similarity scrore . In essence, the engine provides a list of titles that are most similar to the input title. 

Here's some insight into the formula for cosine similarity :

![image](https://github.com/KhaiHuy123/movie-recommendation-system/assets/86825653/b87919aa-6534-4a22-9e84-6d2fc48fb276)

- Tutorial :

To use the search engine, simply enter the name of the movie you're looking for into the entry field. The system will then recommend a list of 7 movie titles that are most similar.

The range for the "lowest point" parameter is from 0.0 to 5.0. This value represents the minimum acceptable rating point. After selecting a point, you can view detailed information about each movie in the recommended list (detailes information not included fully here).

You can use "Advanced Search" functionality to find not only recommedations having closest relationship with the movie you want to search but also the movie recommended by orther users base on rating rate    

- Conclusion : I hope you find this project enjoyable and insightful. If you have any questions or need further assistance, feel free to contact me at  : nkhuy1109@gmail.com

- Demo :

![image](https://github.com/KhaiHuy123/movie-recommendation-system/assets/86825653/492f78c1-e0b9-4747-8ac1-3393e7436b34)

Detailed information of 4th movie in list of 7  :

![image](https://github.com/KhaiHuy123/movie-recommendation-system/assets/86825653/49d7d752-6f93-4a40-a264-5c95ae7ebda8)

You can view recommended movies by clicking Advanced Search button , system will give you list of 7 movies base on "rating rate" of similar users who voted for the movie you are looking for . 

For example, the recommedations for similar moive of "catch me if you can" are :

![image](https://github.com/KhaiHuy123/movie-recommendation-system/assets/86825653/b658135b-2105-410d-86bf-4f44bf8ff5dc)

You can try another movie like :

![image](https://github.com/KhaiHuy123/movie-recommendation-system/assets/86825653/1c02de75-1311-48da-89cb-3559cb25cc2a)

Detailed information of 1st movie in list of 7  :

![image](https://github.com/KhaiHuy123/movie-recommendation-system/assets/86825653/777945bf-abdf-4beb-af60-a7bd5971e483)

Recommended movies :

![image](https://github.com/KhaiHuy123/movie-recommendation-system/assets/86825653/bccca0da-25b8-4496-982e-3682e4629ba7)

-------

Summary
=======

This dataset (ml-25m) describes 5-star rating and free-text tagging activity from [MovieLens](http://movielens.org), a movie recommendation service. It contains 25000095 ratings and 1093360 tag applications across 62423 movies. These data were created by 162541 users between January 09, 1995 and November 21, 2019. This dataset was generated on November 21, 2019.

Users were selected at random for inclusion. All selected users had rated at least 20 movies. No demographic information is included. Each user is represented by an id, and no other information provided.

The data are contained in the files `genome-scores.csv`, `genome-tags.csv`, `links.csv`, `movies.csv`, `ratings.csv` and `tags.csv`. More details about the contents and use of all these files follows.

This and other GroupLens data sets are publicly available for download at <http://grouplens.org/datasets/>.


Usage License
=============

Neither the University of Minnesota nor any of the researchers involved can guarantee the correctness of the data, its suitability for any particular purpose, or the validity of results based on the use of the data set. The data set may be used for any research purposes under the following conditions:

* The user may not state or imply any endorsement from the University of Minnesota or the GroupLens Research Group.
* The user must acknowledge the use of the data set in publications resulting from the use of the data set (see below for citation information).
* The user may not redistribute the data without separate permission.
* The user may not use this information for any commercial or revenue-bearing purposes without first obtaining permission from a faculty member of the GroupLens Research Project at the University of Minnesota.
* The executable software scripts are provided "as is" without warranty of any kind, either expressed or implied, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose. The entire risk as to the quality and performance of them is with you. Should the program prove defective, you assume the cost of all necessary servicing, repair or correction.

In no event shall the University of Minnesota, its affiliates or employees be liable to you for any damages arising out of the use or inability to use these programs (including but not limited to loss of data or data being rendered inaccurate).

If you have any further questions or comments, please email <grouplens-info@umn.edu>


Citation
========

To acknowledge use of the dataset in publications, please cite the following paper:

> F. Maxwell Harper and Joseph A. Konstan. 2015. The MovieLens Datasets: History and Context. ACM Transactions on Interactive Intelligent Systems (TiiS) 5, 4: 19:1–19:19.                         
<https://doi.org/10.1145/2827872>


Further Information About GroupLens
===================================

GroupLens is a research group in the Department of Computer Science and Engineering at the University of Minnesota. Since its inception in 1992, GroupLens's research projects have explored a variety of 
fields including:

* recommender systems
* online communities
* mobile and ubiquitious technologies
* digital libraries
* local geographic information systems

GroupLens Research operates a movie recommender based on collaborative filtering, MovieLens, which is the source of these data. We encourage you to visit <http://movielens.org> to try it out! If you 
have exciting ideas for experimental work to conduct on MovieLens, send us an email at <grouplens-info@cs.umn.edu> - we are always interested in working with external collaborators.


Content and Use of Files
========================

Verifying the Dataset Contents
------------------------------

We encourage you to verify that the dataset you have on your computer is identical to the ones hosted at [grouplens.org](http://grouplens.org).  This is an important step if you downloaded the dataset 
from a location other than [grouplens.org](http://grouplens.org), or if you wish to publish research results based on analysis of the MovieLens dataset.

We provide a [MD5 checksum](http://en.wikipedia.org/wiki/Md5sum) with the same name as the downloadable `.zip` file, but with a `.md5` file extension. To verify the dataset:

    # on linux
    md5sum ml-25m.zip; cat ml-25m.zip.md5

    # on OSX
    md5 ml-25m.zip; cat ml-25m.zip.md5

    # windows users can download a tool from Microsoft (or elsewhere) that verifies MD5 checksums

Check that the two lines of output contain the same hash value.


Formatting and Encoding
-----------------------

The dataset files are written as [comma-separated values](http://en.wikipedia.org/wiki/Comma-separated_values) files with a single header row. Columns that contain commas (`,`) are escaped using double- 
quotes (`"`). These files are encoded as UTF-8. If accented characters in movie titles or tag values (e.g. Misérables, Les (1995)) display incorrectly, make sure that any program reading the data, such 
as a text editor, terminal, or script, is configured for UTF-8.


User Ids
--------

MovieLens users were selected at random for inclusion. Their ids have been anonymized. User ids are consistent between `ratings.csv` and `tags.csv` (i.e., the same id refers to the same user across the 
two files).


Movie Ids
---------

Only movies with at least one rating or tag are included in the dataset. These movie ids are consistent with those used on the MovieLens web site (e.g., id `1` corresponds to the URL 
<https://movielens.org/movies/1>). Movie ids are consistent between `ratings.csv`, `tags.csv`, `movies.csv`, and `links.csv` (i.e., the same id refers to the same movie across these four data files).


Ratings Data File Structure (ratings.csv)
-----------------------------------------

All ratings are contained in the file `ratings.csv`. Each line of this file after the header row represents one rating of one movie by one user, and has the following format:

    userId,movieId,rating,timestamp

The lines within this file are ordered first by userId, then, within user, by movieId.

Ratings are made on a 5-star scale, with half-star increments (0.5 stars - 5.0 stars).

Timestamps represent seconds since midnight Coordinated Universal Time (UTC) of January 1, 1970.


Tags Data File Structure (tags.csv)
-----------------------------------

All tags are contained in the file `tags.csv`. Each line of this file after the header row represents one tag applied to one movie by one user, and has the following format:

    userId,movieId,tag,timestamp

The lines within this file are ordered first by userId, then, within user, by movieId.

Tags are user-generated metadata about movies. Each tag is typically a single word or short phrase. The meaning, value, and purpose of a particular tag is determined by each user.

Timestamps represent seconds since midnight Coordinated Universal Time (UTC) of January 1, 1970.


Movies Data File Structure (movies.csv)
---------------------------------------

Movie information is contained in the file `movies.csv`. Each line of this file after the header row represents one movie, and has the following format:

    movieId,title,genres

Movie titles are entered manually or imported from <https://www.themoviedb.org/>, and include the year of release in parentheses. Errors and inconsistencies may exist in these titles.

Genres are a pipe-separated list, and are selected from the following:

* Action
* Adventure
* Animation
* Children's
* Comedy
* Crime
* Documentary
* Drama
* Fantasy
* Film-Noir
* Horror
* Musical
* Mystery
* Romance
* Sci-Fi
* Thriller
* War
* Western
* (no genres listed)


Links Data File Structure (links.csv)
---------------------------------------

Identifiers that can be used to link to other sources of movie data are contained in the file `links.csv`. Each line of this file after the header row represents one movie, and has the following format:

    movieId,imdbId,tmdbId

movieId is an identifier for movies used by <https://movielens.org>. E.g., the movie Toy Story has the link <https://movielens.org/movies/1>.

imdbId is an identifier for movies used by <http://www.imdb.com>. E.g., the movie Toy Story has the link <http://www.imdb.com/title/tt0114709/>.

tmdbId is an identifier for movies used by <https://www.themoviedb.org>. E.g., the movie Toy Story has the link <https://www.themoviedb.org/movie/862>.

Use of the resources listed above is subject to the terms of each provider.


Tag Genome (genome-scores.csv and genome-tags.csv)
-------------------------------------------------

This data set includes a current copy of the Tag Genome.

[genome-paper]: http://files.grouplens.org/papers/tag_genome.pdf

The tag genome is a data structure that contains tag relevance scores for movies.  The structure is a dense matrix: each movie in the genome has a value for *every* tag in the genome.

As described in [this article][genome-paper], the tag genome encodes how strongly movies exhibit particular properties represented by tags (atmospheric, thought-provoking, realistic, etc.). The tag 
genome was computed using a machine learning algorithm on user-contributed content including tags, ratings, and textual reviews.

The genome is split into two files.  The file `genome-scores.csv` contains movie-tag relevance data in the following format:

    movieId,tagId,relevance

The second file, `genome-tags.csv`, provides the tag descriptions for the tag IDs in the genome file, in the following format:

    tagId,tag

The `tagId` values are generated when the data set is exported, so they may vary from version to version of the MovieLens data sets.

Please include the following citation if referencing tag genome data:

> Jesse Vig, Shilad Sen, and John Riedl. 2012. The Tag Genome: Encoding Community Knowledge to Support Novel Interaction. ACM Trans. Interact. Intell. Syst. 2, 3: 13:1–13:44. 
<https://doi.org/10.1145/2362394.2362395>


Cross-Validation
----------------

Prior versions of the MovieLens dataset included either pre-computed cross-folds or scripts to perform this computation. We no longer bundle either of these features with the dataset, since most modern 
toolkits provide this as a built-in feature. If you wish to learn about standard approaches to cross-fold computation in the context of recommender systems evaluation, see [LensKit](http://lenskit.org) 
for tools, documentation, and open-source code examples.


