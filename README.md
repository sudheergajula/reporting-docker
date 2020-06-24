# Docker-compose files for a simple uptodate
# InfluxDB + Graphite

To start stack
```
./run.sh 
```

We have custom influxdb.conf to enable all Line Protocol format metrics arriving into Influx database. Influx will assume that metrics are coing through graphite.

Ensure that plugin is enabled in influxdb.conf and also enable batching and caching for better performance.

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

Additionally you can also import JSON model to view all metrics instead of creating panels.
```
Check for Grafana instance up and running at 3000 port.
Go to Create(+) => Import and then import Json file import.json
This will load all required panels and you can modify it according to your needs
```

