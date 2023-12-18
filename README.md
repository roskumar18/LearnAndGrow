# LearnAndGrow

#set volume to map to solr container folder in docker compose override, here we will update the changes in configset
- ${LOCAL_DATA_PATH}\epsolrconfigs:C:\solr\server\solr\configsets\epsolrconfigs

#Download config set which you want to modify
.\solr zk downconfig -z localhost:9983 -n sitecore_master_index_config -d C:\solr\server\solr\configsets\epsolrconfigs\sitecore_master_index_config


#update configset in solr via zookeeper
.\solr zk upconfig -z localhost:9983 -n sitecore_master_index_config -d C:\solr\server\solr\configsets\epsolrconfigs\sitecore_master_index_config
