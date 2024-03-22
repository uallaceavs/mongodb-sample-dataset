# [MongoDB Sample Dataset](https://docs.atlas.mongodb.com/sample-data/available-sample-datasets/)

For `mongoimport` the MongoDB database tools need to installed. You can find it [here](https://www.mongodb.com/try/download/database-tools?tck=docs_databasetools)

> this is a fork of [repo](https://github.com/mcampo2/mongodb-sample-databases).

> the original repo has BSON dump. I've removed it and I added a bash [script](https://github.com/neelabalan/mongodb-sample-dataset/blob/main/script.sh) to import the JSON to respective db 

Atlas provides sample data you can load into your Atlas clusters. You can use this data to quickly get started experimenting with data in MongoDB and using tools such as the Atlas Perform CRUD Operations in Atlas and MongoDB Charts.

MongoDB does not provide any sample databases on their website, However, they do provide sample databases for their cloud service Atlas.  These databases have been dumped from a MongoDB Atlas cluster using the MongoDB Compass GUI.  There are 7 databases, with each database collection (table) stored in a seperate JSON file.  These files will accelerate learning of MongoDB's features by allowing new developers to quickly experiment with prepopulated datasets.


## Sample Datasets

| Dataset Name                                                                                | Description                                                       | Collections                                                                |
| ------------------------------------------------------------------------------------------- | ----------------------------------------------------------------- | -------------------------------------------------------------------------- |
| [Sample AirBnB Listings Dataset](https://docs.atlas.mongodb.com/sample-data/sample-airbnb/) | Contains details on AirBnB listings.                              | listingsAndReviews                                                         |
| [Sample Analytics Dataset](https://docs.atlas.mongodb.com/sample-data/sample-analytics/)    | Contains training data for a mock financial services application. | accounts, customers, transactions                                          |
| [Sample Geospatial Dataset](https://docs.atlas.mongodb.com/sample-data/sample-geospatial/)  | Contains shipwreck data.                                          | shipwrecks                                                                 |
| [Sample Mflix Dataset](https://docs.atlas.mongodb.com/sample-data/sample-mflix/)            | Contains movie data.                                              | comments, movies, theaters, users                                          |
| [Sample Supply Store Dataset](https://docs.atlas.mongodb.com/sample-data/sample-supplies/)  | Contains data from a mock office supply store.                    | sales                                                                      |
| [Sample Training Dataset](https://docs.atlas.mongodb.com/sample-data/sample-training/)      | Contains MongoDB training services dataset.                       | companies, grades, inspection, posts, routes, stories, trips, tweets, zips |
| [Sample Weather Dataset](https://docs.atlas.mongodb.com/sample-data/sample-weather/)        | Contains detailed weather reports.                                | data                                                                       |

## Running in docker

```bash
docker pull mvertes/alpine-mongo

docker run -d --name mongo -p 2717:27017 -v ~/mongodb:/data/db mvertes/alpine-mongo

# args
#   hostname   
#   port
./script.sh localhost 2717

# start mongo shell
docker exec -it mongo mongo
```

Based on the provided text, you can see a list of available MongoDB sample databases in this forked GitHub repository:

sample_airbnb
sample_analytics
sample_geospatial
sample_mflix
sample_supplies
sample_training
sample_weatherdata
You can load these sample databases using the provided .json files or the docker-compose file.

To load the sample_mflix database, you can follow the steps provided in the previous question. Here are the steps to summarize it:

Create a new database and collection using the MongoDB Compass:
Name of the database: mflixdb
Name of the collection: filmes
Import the movies.json file:
Click ADD DATA > Import File
Select the movies.json file
Click Import
You can follow the same steps for other databases using their respective JSON files available in the forked GitHub repository.

After you've imported the JSON file, you can verify the data by clicking the filmes collection in the mflixdb database.

You can also use the provided docker-compose file and script.sh file to load the data using Docker. The following steps show you how to do it:

Run this command to pull the MongoDB Docker image:
Edit
Full Screen
Copy code
docker pull mvertes/alpine-mongo
Run this command to start the MongoDB Docker container:
css
Edit
Full Screen
Copy code
docker run -d --name mongo -p 2717:27017 -v ~/mongodb:/data/db mvertes/alpine-mongo
Run the provided script.sh file with the proper arguments:
bash
Edit
Full Screen
Copy code
./script.sh localhost 2717
Finally, you can start the MongoDB shell:
Edit
Full Screen
Copy code
docker exec -it mongo mongo
Now you can access the MongoDB database and query the
