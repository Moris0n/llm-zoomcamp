# Home work week 1

## Q1. Running Elastic  
Run Elastic Search 8.4.3, and get the cluster information. If you run it on localhost, this is how you do it:  
What's the version.build_hash value?  
 curl localhost:9200
{
  "name" : "d81af46cd4be",
  "cluster_name" : "docker-cluster",
  "cluster_uuid" : "uiG4SH-zQzu8V_PqycgVtw",
  "version" : {
    "number" : "8.4.3",
    "build_flavor" : "default",
    "build_type" : "docker",
    "build_hash" : "42f05b9372a9a4a470db3b52817899b99a76ee73",
    "build_date" : "2022-10-04T07:17:24.662462378Z",
    "build_snapshot" : false,
    "lucene_version" : "9.3.0",
    "minimum_wire_compatibility_version" : "7.17.0",
    "minimum_index_compatibility_version" : "7.0.0"
  },
  "tagline" : "You Know, for Search"  

Answer 1 :  
  "build_hash" : "42f05b9372a9a4a470db3b52817899b99a76ee73"

## Q2. Indexing the data
Index the data in the same way as was shown in the course videos. Make the course field a keyword and the rest should be text.  

Which function do you use for adding your data to elastic?

''' es_client.index(index=index_name, document=doc)'''

Answer 2: index

## Q3. Searching
Now let's search in our index.

For a query "How do I execute a command in a running docker container?", what's the score for the top ranking result?

Use only question and text fields and give question a boost of 4

Answer 3 : 84.05
## Q4. Filtering
Now let's only limit the questions to machine-learning-zoomcamp.

Return 3 results. What's the 3rd question returned by the search engine?  

Answer 4 : How do I copy files from a different folder into docker container’s working directory?

## Q5. Building a prompt
What's the length of the result? (use the len function)

1462