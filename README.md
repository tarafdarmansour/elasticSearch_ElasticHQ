# elasticSearch_ElasticHQ
Here, you can run elasticsearch docker and monitor its node\nodes using [elasticsearch-HQ](https://github.com/ElasticHQ/elasticsearch-HQ)


## To run elasticSearch whith 3 nodes and ElasticHQ
````
docker-compose -f .\docker-compose-3nodes.yml up
````
to connect elasticsearch in ElasticHQ first page you should address elasticsearch node servicename that exposed 9200 port
![alt text](https://github.com/tarafdarmansour/elasticSearch_ElasticHQ/blob/main/readmeimages/ElasticHQ_3nodes.png "ElasticHQ first page configuration for multiple node")


## To run elasticSearch whith single node and ElasticHQ
````
docker-compose -f .\docker-compose-singlenode.yml up
````
to connect elasticsearch in ElasticHQ first page you should address elasticsearch servicename
![alt text](https://github.com/tarafdarmansour/elasticSearch_ElasticHQ/blob/main/readmeimages/ElasticHQ_singlenode.png "ElasticHQ first page configuration")



## To JUST run elasticSearch whith single node 
````
docker run --name elasticsearch_container -p 9200:9200 -p 9300:9300 -e "discovery.type=single-node" elasticsearch:7.12.1
````

## To JUST run  ElasticHQ
````
docker run --name elasticsearch-hq_container -p 5000:5000 elastichq/elasticsearch-hq
````
to connect elasticsearch in ElasticHQ first page you should address elasticsearch on localhost than is host.docker.internal
![alt text](https://github.com/tarafdarmansour/elasticSearch_ElasticHQ/blob/main/readmeimages/ElasticHQ_host.png "ElasticHQ first page configuration for localhost")

