# Split routing demo

>RE: https://github.com/open-telemetry/opentelemetry-collector-contrib/issues/6920
Based on: https://github.com/open-telemetry/opentelemetry-collector-contrib/tree/main/examples/demo

## Metrics

`server` emits two metrics:

* `demo_server_request_counts_high_value`, annotated with:
    * `"metric-value": "high"`
    * `"X-Custom-Metrics-Header": "business-critical"`

* `demo_server_request_counts_low_value`, annotated with:
    * `"metric-value": "low"`

## Usage

`docker-compose up -d` to run.

`docker-compose down` to delete.

### Prometheus UI

* Prometheus (http://localhost:9090): `kubectl port-forward svc/prometheus 9090:9090`
* Prometheus/hc (http://localhost:9091): `kubectl port-forward svc/prometheus-hc 9091:9091`


