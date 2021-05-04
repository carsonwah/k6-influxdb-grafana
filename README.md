# k6-influxdb-grafana

## Getting Started

```bash
# Start influxdb and grafana services
docker-compose up -d

# Run load test and store result to "k6" database
docker run -i --network container:influxdb loadimpact/k6 run --vus 10 --duration 10s --out influxdb=http://influxdb:8086/k6 --tag APP_NAME=EPTH_WEBAPP --tag APP_VERSION=1.0.0 - <perf-test.js

# Access localhost:3000 to view result in Grafana dashboard
# Sample dashboard: https://grafana.com/grafana/dashboards/2587
```

## References

- https://github.com/k6io/k6
- https://github.com/jkehres/docker-compose-influxdb-grafana
