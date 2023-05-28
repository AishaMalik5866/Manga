# Manga
A table and some queries I created of a few volumes of manga (Japanese comic books) by Gege or Togashi- originally created on Khan Academy while learning SQL


CREATE TABLE manga (id INTEGER PRIMARY KEY, name TEXT, volume INTEGER, language TEXT, author TEXT, chapters INTEGER, price INTEGER);

INSERT INTO manga VALUES (1, "Hunter X Hunter", 7, "English", "Togashi", 9, 10.99);
INSERT INTO manga VALUES (2, "Hunter X Hunter", 4, "Japanese", "Togashi", 9, 9.99);
INSERT INTO manga VALUES (3, "Hunter X Hunter", 15, "English", "Togashi", 10, 9.99);
INSERT INTO manga VALUES (4, "Hunter X Hunter", 11, "Japanese", "Togashi", 9, 10.99);
INSERT INTO manga VALUES (5, "Hunter X Hunter", 13, "Japanese", "Togashi", 9, 9.99);
INSERT INTO manga VALUES (6, "Jujutsu Kaisen", 3, "English", "Gege", 7, 8.99);
INSERT INTO manga VALUES (7, "Jujutsu Kaisen", 2, "English", "Gege", 8, 8.99);
INSERT INTO manga VALUES (8, "Jujutsu Kaisen", 1, "English", "Gege", 8, 9.99);
INSERT INTO manga VALUES (9, "Jujutsu Kaisen", 5, "English", "Gege", 9, 9.99);
INSERT INTO manga VALUES (10, "Jujutsu Kaisen", 4, "Japanese", "Gege", 7, 8.99);
INSERT INTO manga VALUES (11, "YuYu Hakusho", 6, "Japanese", "Togashi", 8, 8.99);
INSERT INTO manga VALUES (12, "YuYu Hakusho", 10, "Japanese", "Togashi", 8, 8.99);
INSERT INTO manga VALUES (13, "YuYu Hakusho", 8, "Japanese", "Togashi", 8, 8.99);
INSERT INTO manga VALUES (14, "YuYu Hakusho", 7, "Japanese", "Togashi", 8, 8.99);
INSERT INTO manga VALUES (15, "YuYu Hakusho", 9, "Japanese", "Togashi", 8, 8.99);

SELECT * FROM manga;

SELECT * FROM manga ORDER BY price;

SELECT SUM(chapters) FROM manga WHERE name = "Hunter X Hunter";

SELECT SUM(price) FROM manga WHERE author = "Togashi";

SELECT name, SUM(price) FROM manga GROUP BY name;

SELECT id, name, volume, language, price FROM manga ORDER BY language;

SELECT * FROM manga ORDER BY chapters;

SELECT * FROM manga ORDER BY name;

SELECT * FROM manga WHERE language = "Japanese" and price < 10;

SELECT * FROM manga WHERE language = "English" and chapters = 9;

SELECT * FROM manga WHERE name = "Jujutsu Kaisen" and language = "English";

SELECT * FROM manga WHERE NOT author = "Togashi";

SELECT * FROM manga WHERE language="Japanese" ORDER BY volume DESC;

SELECT SUM(price) FROM manga WHERE NOT author="Gege";
