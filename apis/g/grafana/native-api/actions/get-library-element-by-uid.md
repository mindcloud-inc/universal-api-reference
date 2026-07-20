# Get Library Element By UID with Grafana

Retrieves a library element from Grafana by UID.

## Endpoint

- **Method:** `GET`
- **Path:** `/library-elements/:library_element_uid`
- **Base URL:** `https://apps78aa.grafana.net/api`
- **Official documentation:** [Get Library Element By UID](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/library_element/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `library_element_uid` | path | `string` | yes | The library element UID. |
