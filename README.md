# prometheus-grafana-dashboard
Docker-compose file for deploying grafana and Prometheus along with Convoy. Also, grafana dashboards for observing queue and consumer metrics.

## Usage. 
1. Clone the convoy [repo](https://github.com/frain-dev/convoy). Change directory into the repo and create a docker-compose.yml file.
2. Copy the contents of [docker-compose.yml](./docker-compose.yml) and paste into your own file and save.
3. If you want, you can modify the compose file to use an already existing convoy image from [Github Container Registry](https://github.com/frain-dev/convoy/pkgs/container/convoy).  
4. You'll need to also create your convoy.json config file but there is a sample config here that works [convoy.json](./convoy.json).  
5. Note that the convoy.json config here is using Redis and Mongo, so the compose file deploys redis and mongo along with convoy.  
6. Build and run the containers.
```bash
docker-compose up -d
```
7. Once the build is complete, go to localhost:3000 to view your grafana instance. 
8. You can import the sample [dashboards](./dashboards) into your grafana instance. 
