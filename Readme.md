1--------------------------------------------------------

clone the repo

TO use the repo to restore mongo db 

docker cp mongo_bkp <mongo_container_id>:/data/restore

docker exec <mongo_container_id> mongostore /data/restore

2-------------------------------------------------------

TO backup mongo db data again

docker exec <mongo_container_id> mongodump --out /data/backup

docker cp <mongo_container_id>:/data/backup ./mongo_bkp

commit and push to repo

