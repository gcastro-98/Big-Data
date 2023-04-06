# ``docker-compose`` hands on: San Diego food truck example

git clone https://github.com/rohit-nlp/FoodTruckExample
cd FoodTrucksExample

## We make the backend work with ElasticSearch (it will listen to ports 9200 & 9300)

docker pull docker.elastic.co/elasticsearch/elasticsearch:6.3.2
docker run -d --name es -p 9200:9200 -p 9300:9300 -e "discovery.type=single-node" docker.elastic.co/elasticsearch/elasticsearch:6.3.2

## Now we set up the frontend using flask (Python & NodeJS)

docker build -t rohit1308k/foodtrucks-web .
docker run -P --rm rohit1308k/foodtrucks-web
