Return ALL the data in the 'movies' table.
SELECT * FROM movies

Return ONLY the name column from the 'people' table
SELECT name FROM people

Oops! Someone spelled Krusty The Clown's name wrong! Change it to reflect the proper spelling (Crusty should be Krusty).
UPDATE people
SET name = 'Krusty the Clown'
WHERE id = 13

Return ONLY Homer Simpson's name from the 'people' table.
SELECT name FROM people
WHERE id = 1

The cinema is showing 'Batman Begins', but Batman is DC, not Marvel! Delete the entry from the 'movies' table.
DELETE from movies
WHERE id = 9


We forgot one of the main characters! Add Bart Simpson to the 'people' table

INSERT INTO people (name)
VALUES ('Bart Simpson')


Eric Cartman has decided to hijack our movie evening, Remove him from the table of people.
DELETE from people
WHERE id = 11


The cinema has just heard that they will be holding an exclusive midnight showing of 'Avengers: Infinity War'!! Create a new entry in the 'movies' table to reflect this.
INSERT INTO movies (title, year, show_time)
VALUES ('Avengers: Infinity War', 2018, '00:00')

The cinema would like to make the Iron Man movies a triple billing. Find out the show time of "Iron Man 2" and set the show time of "Iron Man 3" to start two hours later.

<!-- not working but I'm thinking something like -->
SET show_time = EXTRACT (show_time FROM movie WHERE id = 3 + interval '2 hours')
WHERE id = 7
