# influxsetup

influxdb configs

```
sudo docker network create influxdb
sudo docker run -d -p 8086:8086 --name=influxdb -v /var/lib/influxdb:/var/lib/influxdb -v /etc/influxdb/influxdb.conf:/etc/influxdb/influxdb.conf:ro influxdb -config /etc/influxdb/influxdb.conf
sudo docker run --name=telegraf -v /etc/telegraf/telegraf.conf:/etc/telegraf/telegraf.conf:ro telegraf
sudo docker run --rm --name=telegraf -v /etc/telegraf/telegraf.conf:/etc/telegraf/telegraf.conf:ro telegraf
sudo docker run -d  -v /var/lib/grafana:/var/lib/grafana --name=grafana -p 3000:3000 grafana/grafana
```
