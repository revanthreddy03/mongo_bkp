*---------------------------------------------------

TO run a mongo docker container

sudo docker run -d -p 27017:27017 mongo



1--------------------------------------------------------

clone the repo

TO use the repo to restore mongo db  (HINT:use 'sudo' before cmds if permission denied)

docker cp mongo_bkp <mongo_container_id>:/data/restore

docker exec <mongo_container_id> mongorestore /data/restore


2-------------------------------------------------------

TO backup mongo db data again   (HINT:use 'sudo' before cmds if permission denied)

docker exec <mongo_container_id> mongodump --out /data/backup

docker cp <mongo_container_id>:/data/backup ./mongo_bkp

commit and push to repo






