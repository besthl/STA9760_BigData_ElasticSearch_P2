# STA9760 Project 2 Part 2---Loading Data into ElasticSearch
In this part, we want leverage docker-compose to bring up a service that encapsulates the bigdata1 container and an elasticsearch container and ensures that they are able to interact. 
In order to interact with elasticsearch in python, PyPI’s elasticsearch module ought to be used. Additionally, all elasticsearch related logic should be wrapped into an internal module that lives within the src folder in this project.

## Start:

docker-compose up -d


This will start ElasticSearch and Kibana.

ElasticSearch: http://localhost:9200 Kibana: http://localhost:5601


Running python:

export APP_KEY={MY_TOKEN}

docker-compose run pyth python parking.py --page_size=1000 --num_pages=4


export curl output:

curl -X GET {localhost:9200/parking-violation-index} > output.txt


Shutting off:

docker-compose down
