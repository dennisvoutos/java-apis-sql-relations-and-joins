# Schema for the database.


## Let's look at the data shown below as a single monolithic table.

| ID | Title                 | Director               | Director Country | Star              | Star DOB   | Writer                   | Writer Email          | Year | Genre           | Score |
|----|-----------------------|------------------------|------------------|-------------------|------------|--------------------------|-----------------------|------|-----------------|-------|
| 1  | 2001: A Space Odyssey | Stanley Kubrick        | USA              | Keir Dullea       | 30/05/1936 | Arthur C Clarke          | arthur@clarke.com     | 1968 | Science Fiction | 10    |
| 2  | Star Wars: A New Hope | George Lucas           | USA              | Mark Hamill       | 25/09/1951 | George Lucas             | george@email.com      | 1977 | Science Fiction | 7     |
| 3  | To Kill A Mockingbird | Robert Mulligan        | USA              | Gregory Peck      | 05/04/1916 | Harper Lee               | harper@lee.com        | 1962 | Drama           | 10    |
| 4  | Titanic               | James Cameron          | Canada           | Leonardo DiCaprio | 11/11/1974 | James Cameron            | james@cameron.com     | 1997 | Romance         | 5     |
| 5  | Dr Zhivago            | David Lean             | UK               | Julie Christie    | 14/04/1940 | Boris Pasternak          | boris@boris.com       | 1965 | Historical      | 8     |
| 6  | El Cid                | Anthony Mann           | USA              | Charlton Heston   | 04/10/1923 | Frederick Frank          | fred@frank.com        | 1961 | Historical      | 6     |
| 7  | Voyage to Cythera     | Theodoros Angelopoulos | Greece           | Manos Katrakis    | 14/08/1908 | Theodoros Angelopoulos   | theo@angelopoulos.com | 1984 | Drama           | 8     |
| 8  | Soldier of Orange     | Paul Verhoeven         | Netherlands      | Rutger Hauer      | 23/01/1944 | Erik Hazelhoff Roelfzema | erik@roelfzema.com    | 1977 | Thriller        | 8     |
| 9  | Three Colours: Blue   | Krzysztof Kieslowski   | Poland           | Juliette Binoche  | 09/03/1964 | Krzysztof Kieślowski     | email@email.com       | 1993 | Drama           | 8     |
| 10 | Cyrano de Bergerac    | Jean-Paul Rappeneau    | France           | Gerard Depardieu  | 27/12/1948 | Edmond Rostand           | edmond@rostand.com    | 1990 | Historical      | 9     |

## We want to normalise the data shown in the table so that it has multiple tables (Film, Director, Star and Writer). Below are the listed tables:

### Director
| ID | Name | Country |
|----|------|---------|

### Star
| ID | Name | DOB |
|----|------|-----|

### Writer

| ID | Name | email |
|----|------|-------|

### Film

| ID | Title | Director_id | Star_id | Writer_id | Year | Genre | Score |
|----|-------|-------------|---------|-----------|------|-------|-------|

#### In the sql file called "create-tables.sql" is the code for creating the tables and in the file "fill-tables.sql" is the code for filling those tables.


