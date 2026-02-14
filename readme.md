# InfluxDb 2

https://github.com/BenJ1337/docker_ha_home-assistant-bootstrap

```
# mkdir -p ./influxdb3/data
# mkdir -p ./influxdb3/plugins
# chmod -R 777 ./influxdb3/
```

```
$ docker exec -it ha-influxdb influxdb3 create token --admin
$ docker exec -it ha-influxdb influxdb3 create database --retention-period 10y ha --token apiv3_st8H9gptgJL3bFp3uQ_UW0vmLlGiLITLfp5LgTKMIlzRh6hdX0mubCzzgTvzH2lRaQeLFVaNKCzIZwEnv_r6eA```
```

# UI

```
docker run --rm \
  --name influxdb3-explorer \
  --publish 8888:80 \
  --publish 8889:8888 \
  influxdata/influxdb3-ui:1.0.0 \
  --mode=admin
```
