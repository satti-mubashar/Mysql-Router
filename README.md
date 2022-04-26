# Mysql-Router

Commands to deploy mysql statefulset

kubectl apply -f mysql-statefulset.yml

after successfully runnin of pods, we have to create cluster
run following commands 1 by 1


mysqlsh --uri='root:root@db-0.mysql'
var cluster = dba.createCluster('mysql');

cluster.addInstance('root:root@db-1.mysql');
cluster.addInstance('root:root@db-2.mysql');
cluster.status();


kubectl apply -f mysql-router-deployment.yml
