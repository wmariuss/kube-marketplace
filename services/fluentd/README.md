# Fluentd

Deploy and manage Fluentd.

## Requirements

* Elasticsearch credentials

## Deploy

1. Change `secret.yml` file with your elasticsearch credentials data
2. Filebeat deploy: `kubectl apply -k .`
