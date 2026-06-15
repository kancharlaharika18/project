# project
movie database system
PROJECT REPORT
MOVIE DATABASE MANAGEMENT SYSTEM
Submitted by
Harika
SUBMITTED TO
B.CHINNA KESHAVA REDDY
ABSTRACT:
The Movie Database Management System is designed to efficiently store, organize, and
manage data related to movie production using a relational database approach. The system
maintains structured information about movies, producers, directors, actors, genres, shooting
locations, technical crew, and promotional activities. By organizing data into multiple
interrelated tables, the project ensures data integrity, reduces redundancy, and supports
accurate data retrieval. This project demonstrates the practical application of database design
concepts such as entity relationships, primary keys, and foreign keys. Overall, the system
provides a scalable and reliable solution for managing complex movie industry data in an
organized manner.
INDEX
1. Introduction
2. Project Objective
3. Tools and Technologies Used
4. Database Design
4.1 Description of Tables
4.2 Relationships Between Tables
4.3 ER Diagram
5. Functional Overview of the System
6. Advantages of the System
7. Conclusion
1. Introduction
The Movie Database Management System is designed to manage and organize detailed
information related to movies and their production process.
The film industry involves multiple entities such as producers, directors, actors, locations,
genres, promotions, and technical crew. Managing this data manually is complex and
inefficient.
This project uses a relational database approach to store movie-related data in a structured
manner. The system ensures data consistency, reduces redundancy, and enables efficient
retrieval of information using relationships between tables.
2. Project Objective
The objectives of this project are:
• To design a relational database for managing movie production data
• To store structured information about movies, cast, crew, and promotions
• To establish relationships between different entities using keys
• To understand real-world database design through a team-based project
• To apply SQL concepts for academic and practical learning
3. Tools and Technologies Used
• Database Management System: MySQL
• Query Language: SQL
• Database Interface: MySQL Workbench / MySQL Command Line
• Operating System: Windows
4. Database Design
The database is designed using multiple related tables, each representing a real-world entity
involved in movie production. Proper normalization techniques are followed to maintain data
integrity.
Database Name: movie_project
4.1 Description of Tables
1. Producers Table
Stores information about movie producers, including their name, net worth, production house,
and the year they started their career. Each producer can be associated with multiple movies.
2. Directors Table
Contains details of directors such as name, number of films directed, remuneration, and the
producer they are associated with. This table establishes a relationship between directors and
producers.
3. Genre Table
Stores movie genre information along with its category. Each movie is assigned a specific genre
to classify it based on content and theme.
4. Location Table
Maintains details of shooting or production locations, including country, state, and estimated
budget required for shooting at that location.
5. Movie Table
This is the central table of the system. It stores movie details such as movie name and connects
with directors, producers, genres, and locations through foreign key relationships.
6. Actors Table
Stores information about actors including age, gender, role, experience, remuneration, and the
movie they acted in. It also links actors with directors to represent professional collaboration.
7. Set Management Table
Contains data related to set management staff such as art directors, designers, and supervisors.
It records their role, remuneration, materials used, and associated movie and director.
8. Choreographer Table
Stores choreographer details including team name, number of songs choreographed,
experience, dance style, gender, and remuneration. Each choreographer is linked to a specific
movie and director.
9. Photographer Table
Maintains details of photographers such as years of experience, specialization, remuneration,
and the movie they worked on.
10. Promotions Table
Stores information about promotional activities including company name, promotion location,
media type, budget, and the movie being promoted.
4.2 Relationships Between Tables
• A producer can produce multiple movies
• A director can direct multiple movies
• Each movie is associated with one producer, one director, one genre, and one location
• Multiple actors, choreographers, set managers, and photographers can work on the
same movie
• Promotional activities are linked directly to movies
These relationships are implemented using primary keys and foreign keys, ensuring referential
integrity.
4.3 ER Diagram
The ER Diagram visually represents all entities and their relationships in the Movie Database
Management System. It shows how movies act as the central entity connected to producers,
directors, actors, genre, location, and promotional data.
SAMPLE QUERIES:

1. Display all producers
SELECT * FROM producers;
2. Display all directors
SELECT * FROM directors;
3. Display all genres
SELECT * FROM genre;
4. Display all locations
SELECT * FROM location;
5. Display all movies
SELECT * FROM movie;
6. Display all actors
SELECT * FROM actors;
7. Display all set management staff
SELECT * FROM set_management;
8. Display all choreographers
SELECT * FROM choreographer;
9. Display all photographers
SELECT * FROM photographer;
10. Display all promotions
SELECT * FROM promotions;
11. Display movies belonging to a specific genre
SELECT movie_name
FROM movie WHERE genre_id = 5;
12. Display actors with more than 20 years of experience
SELECT name, experience
FROM actors
WHERE experience > 20;
13. Display female actors
SELECT name, role
FROM actors
WHERE gender = 'Female';
14. Display directors who directed more than 15 films
SELECT name, no_of_films_directed
FROM directors
WHERE no_of_films_directed > 15;
15. Display movie name with director name
SELECT m.movie_name, d.name
FROM movie m
JOIN directors d ON m.director_id = d.director_id;
16. Display movie name with producer name
SELECT m.movie_name, p.name
FROM movie m
JOIN producers p ON m.producer_id = p.producer_id;
17. Display actor name with movie name
SELECT a.name, m.movie_name FROM actors a JOIN movie m ON a.movie_id =
m.movie_id;
18. Count total number of movies
SELECT COUNT(*) AS total_movies
FROM movie;
19. Count total number of actors
SELECT COUNT(*) AS total_actors
FROM actors;
20. Find maximum remuneration of actors
SELECT MAX(remuneration) AS highest_paid_actor
FROM actors;
21. Display actors ordered by experience
SELECT name, experience
FROM actors
ORDER BY experience DESC;
22. Display movies ordered by movie name
SELECT movie_name
FROM movie ORDER BY movie_name;
5. Functional Overview of the System
• Stores complete movie production details
• Tracks cast and crew involvement for each movie
• Maintains budget and promotion-related information
• Supports structured data retrieval for analysis
• Enables efficient management of large datasets
6. Advantages of the System
• Eliminates data redundancy
• Ensures data integrity through relationships
• Easy to maintain and update
• Scalable for future expansion
• Reflects real-world movie industry structure
7. Conclusion
The Movie Database Management System successfully demonstrates the application of
relational database concepts in a real-world scenario.
By organizing movie production data into structured tables and defining proper relationships,
the system ensures accuracy, consistency, and efficient data handling.
This project enhanced our understanding of database design, normalization, and teamwork,
making it a valuable academic learning experience.
