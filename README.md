# Lab Assignment. Neo4j

## The Dataset

The dataset that we are using consists of data obtained from MovieLens 1, a recommender system whose users give movies a rate between 1 and 5 based on whether they dislike or love them. MovieLens uses the rates to recommend movies that its users might like. The dataset is modeled as a directed graph and consists of 100,004 rates on 9,125 movies across 671 users between January 9th, 1995 and October 16, 2016. The dataset also contains the names of the directors and the actors of each movie.
A directed graph G = (V , E ) consists of:

- A set V of nodes corresponding to the entities, such as movies, users, actors and direc-
tors.
- A set E of links, each connecting two nodes and representing a relationship between two entities. For instance, a link between a director and a movie represents the rela- tionship “directed by”.


## Preliminaries

You will need to have Docker installed on your computer.
If it is not the case, please [click on this link](https://store.docker.com/). 

In order to use Neo4j, you will need to:

1. Download the dataset
2. Launch the Neo4j server.
3. Launche the client.

### Download the dataset

Open a terminal (Windows users: Command Prompt or PowerShell, but not PowerShell ISE)
and create a directory named neo4j-assignment with the following command:

```
mkdir neo4j-assignment
```

Move to that directory with the following command:

```
cd neo4j-assignment
```

Create a new directory named data with the following command:

```
mkdir data
```

Download the file [graph.zip]() and unzip it in the directory data.

### Launch the Neo4j server

Mac and Linux users, execute the following command:

```
docker run --env=NEO4J_AUTH=none --publish=7474:7474 --volume=$PWD/data:/data neo4j:2.3
```

Windows users, execute the following command:

```
docker run --env=NEO4J_AUTH=none --publish=7474:7474 --volume=%cd%/data:/data neo4j:2.3
```

### Launch the Neo4j client

Just open a browser and type the following URL:

```
http://localhost:7474/browser/
```

## Queries

Write and run the following queries:

1. The genres of the movies in the database. 
2. The number of movies in the database.
3. The title of the movies released in 2005.
4. The number of directors by movie. Sort in decreasing order.
5. The names of the directors and the title of the movies that they directed and in which they also played.
6. The genres of the movies in which Tom Hanks played.
7. The title and the rate of all the movies that the user number 3 
rated. Sort by rate in decreasing order.
8. The five movies that obtained the best average rate among the movies that have been rated by at least 100 users.

