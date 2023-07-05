# lgtm-stack

Grafana's LGTM Stack in a single umbrella helm chart

```
helm upgrade --install -n lgtm lgtm ./ --values values.yaml
```

# TODO

- Both Mimir and Tempo deploy their own Minio, ideally deploying minio would be set to false for those two, then include minio in the top level LGTM stack chart.
- Mimir deploys in multi-tenant mode by default, so that either needs to be false, or, the data source needs to include the x-scope-orgId header.
- add subchart conditions to datasources
