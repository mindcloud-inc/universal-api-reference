# Get Library Element By Name with Grafana

Retrieves a library element from Grafana by name.

## Endpoint

- **Method:** `GET`
- **Path:** `/library-elements/name/:library_element_name`
- **Base URL:** `https://apps78aa.grafana.net/api`
- **Official documentation:** [Get Library Element By Name](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/library_element/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `library_element_name` | path | `string` | yes | The library element name. |
