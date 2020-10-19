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


### reference
```
https://www.youtube.com/watch?v=DzyC8lqbjC8
issue: https://stackoverflow.com/questions/39108992/mongoerror-getaddrinfo-enotfound-undefined-undefined27017
https://phoenixnap.com/kb/docker-mongodb
```
