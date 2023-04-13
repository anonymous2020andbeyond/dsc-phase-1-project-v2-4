# Using Data to Support Microsoft's Original Video Content Venture

**Author**: Jacqueline Du Bois

## Project Overview

This project proposes two ways to support Microsoft's entry into the online video content market.  A descriptive analysis of publicly available movie data shows that the company can either pursue film projects determined by the most popular and profitable genres, or it can hire a director with a diverse portfolio of work collaboratively with the head of Microsoft's new movie studio to design its first venture.  The analysis offers guidance on which genres and directors are most likely to yield a successful film.    

### Business Problem

Microsoft has decided to create a new movie studio, but the executive hired to lead the venture requires support to not only determine what constitutes success at the box office, but also to use that knowledge to scope the seemingly limitless film project options to a limited set that are most likely to produce a successful film.  

![img](./images/director_shot.jpeg)
### The Data

In the folder `zippedData` are movie datasets from:

* [Box Office Mojo](https://www.boxofficemojo.com/)
* [IMDB](https://www.imdb.com/)
* [Rotten Tomatoes](https://www.rottentomatoes.com/)
* [TheMovieDB](https://www.themoviedb.org/)
* [The Numbers](https://www.the-numbers.com/)

This project makes use of the IMDB and The Numbers datasets, only. The IMDB database contains movie characteristics, ratings, and principal role information.  The Numbers dataset contains financial information about the production of a broad range of movies.  Rotten Tomatoes alsoo contains rating data; however, the IMDb ratings database contains many more records and is thus assumed to be the more comprehensive source of this type of information.  Something similar can be said about the Box Office Mojo and The Numbers movie earnings data.  Because this data files needs to be joined in order to provide the insights the Microsoft studio lead requires, it was decided to use the files with the largest number of records to minimize the potential for data loss due to an unbalanced mere.  The data from IMDB is organized in a SQLite database as shown below.

![movie data erd](https://raw.githubusercontent.com/learn-co-curriculum/dsc-phase-1-project-v2-4/master/movie_data_erd.jpeg)

### Methods

This project uses descriptive analysis at the level of the film.  Information with respect to ratings and box office earnings is also aggregated up to the level of a film genre to determine which genres are most frequently associated with the highest rated and highest earning films.

## Results
A successful film is defined as one that has received votes cast, average ratings, and net domestic profits above the average.  

* The genres most frequently associated with films meeting these criteria are most likely to be of the "Mystery", "Crime" and "Adventure" genres.  It must be noted however that generating a film of the "Adventure" genre carries somewhat more risk as it is associated with production budgets 4-5 times greater than the other two genres.

![genre_success_factor](./images/genre_success_factor.png)

* The directors most frequently associated with films of these three genres are: David Fincher, David Villeneuve, Christopher Nolan (highest rating, highest votes), and David O'Russel (highest net domestic profit).

![director_success](./images/director_success.png)

* The directors among the top producers of successful films who could likely work on a wide variety of projects with Microsoft are David Fincher and Christopher Nolan.

## Conclusions

This analysis leads to three recommendations to help Microsoft's new studio lead decide on a film project:
- Focus on genres associated with the most successful movies and moderate financial risk.
- Hire the director most capable of realizing the genres associated with the most successful movies. 
- Hire the director who is familiar with a broad range of genres and could be called upont to support future work. 

## Limitations and Next Steps
Limitations of this approach stem from not using all of the listed genres for a given film.  While this avoided double or triple counting the success factors associated with a given film, it may have under represented certain film genres.  Future work could explore ways of casting the compound genre differently

Additional work could include looking at how certain actors influence the measures of success and what their starring in a film means for that film's return on investment.

## Repository Structure
```
|-- data
|--images
|--zippedData
|--README.md
|--dubois_notebook_v2.pdf
|--presentation.pdf
|--student.ipynb
```
   