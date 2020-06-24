# Docker-compose files for a simple uptodate
# InfluxDB + Graphite

To start stack
```
./run.sh 
```

We have custom influxdb.conf.
Ensure that plugin is enabled

```
[[graphite]]
  # Determines whether the graphite endpoint is enabled.
    enabled = true
    database = "metrics_db"
    retention-policy = ""
    bind-address = ":2003"
    protocol = "tcp"
    consistency-level = "one"
```
