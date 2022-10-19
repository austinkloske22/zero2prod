# zero2prod

## Getting started

starting docker 
```
sudo service docker start
```

create new postgres container
```
./scripts/init_db.sh
```

curl requests
```
curl http://127.0.0.1:8000/health_check y
```
```
curl -i -X POST -d 'email=thomas_mann@hotmail.com&name=Tom' \
http://127.0.0.1:8000/subscriptions
```