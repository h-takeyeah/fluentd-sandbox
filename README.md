fluentd-sandbox
===

sample project with fluentd

* [Config File Syntax (YAML)](https://docs.fluentd.org/configuration/config-file-yaml) (supported by fluentd >= 1.15.0)
* :ng: `FLUENT_CONF`, :ok: `FLUENTD_CONF` ([source](https://github.com/fluent/fluentd-docker-image/issues/227))

Logging example - [HTTP](./conf/http.yml)
---

```sh
docker compose up -d
docker compose logs --follow

# another terminal
curl -d 'json={"json":"message"}' http://127.0.0.1:9880/sample.test
```