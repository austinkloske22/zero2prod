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

building a docker image / running a docker image
```
docker build --tag zero2prod --file Dockerfile .
docker run -p 8000:8000 zero2prod

```

prepare docker build for offline mode (`saves to sqlz-data.json`)
```
cargo sqlx prepare -- --lib
```

curl requests
```
curl -v http://127.0.0.1:8000/health_check
```
```
curl -i -X POST -d 'email=thomas_mann@hotmail.com&name=Tom' \
http://127.0.0.1:8000/subscriptions
```