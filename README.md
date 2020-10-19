## ec2 ubuntu 18.04 install mongo
Run mongo db container 
```
sudo docker run  -p 27017:27017 --name mdb mongo
```

bash into the container and run mongo shell 
```
sudo docker exec -it mdb mongo
```

create a documentary
```
mongo
use test
db.users_test.insertMany([
{
 "name": "hunter",
 "age": 36, 
 "title" : "Engineer"
},
{
 "name": "sarra",
 "age": 24, 
 "title" : "clerk"
}])
```
findOne
```
{
name:"hunter"
}
```

remote ec2  mongodb
```
mongo "54.87.133.19:27017"
mongo -u kaden -p 1234 54.87.133.19/ml-test

54.87.133.19:3000
```

run ui
```
sudo docker run -p 3000:3000 --name mclient mongoclient/mongoclient
```

create user and password
```
db.createUser({
    user: 'kaden',
    pwd: '1234',
    roles: [{ role: 'readWrite', db:'ml-test'}]
})
```

reference
https://medium.com/faun/install-mongodb-on-aws-ubuntu-ec2-instance-6794cd8e3b4e


### more docker 
```
docker stop $(docker ps -aq)    
docker rm $(docker ps -aq)    
docker rmi $(docker images -q)
```

```
sudo docker stop $(sudo docker ps -aq)    
sudo docker rm $(sudo docker ps -aq)    
sudo docker rmi $(sudo docker images -q)
```


### mongoDB1 -> 
```
https://www.youtube.com/watch?v=DzyC8lqbjC8
issue: https://stackoverflow.com/questions/39108992/mongoerror-getaddrinfo-enotfound-undefined-undefined27017
```


### reference
```
https://www.youtube.com/watch?v=DzyC8lqbjC8
issue: https://stackoverflow.com/questions/39108992/mongoerror-getaddrinfo-enotfound-undefined-undefined27017
https://phoenixnap.com/kb/docker-mongodb
```
