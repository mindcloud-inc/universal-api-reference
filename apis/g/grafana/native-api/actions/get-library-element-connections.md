# Get Library Element Connections with Grafana

Retrieves library element connections from Grafana.

## Endpoint

- **Method:** `GET`
- **Path:** `/library-elements/:library_element_uid/connections/`
- **Base URL:** `https://apps78aa.grafana.net/api`
- **Official documentation:** [Get Library Element Connections](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/library_element/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `library_element_uid` | path | `string` | yes | The library element UID. |
