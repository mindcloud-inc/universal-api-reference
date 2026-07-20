# List Host Services with Checkmk

Retrieves monitored service records for a Checkmk host.

## Endpoint

- **Method:** `GET`
- **Path:** `/objects/host/{host_name}/collections/services`
- **Base URL:** `{apiUrl}`
- **Official documentation:** [List Host Services](https://docs.checkmk.com/latest/en/rest_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `host_name` | path | `string` | yes | Checkmk host name. |
