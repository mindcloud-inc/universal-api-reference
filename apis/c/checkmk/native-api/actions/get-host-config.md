# Get Host Config with Checkmk

Retrieves host configuration details from Checkmk.

## Endpoint

- **Method:** `GET`
- **Path:** `/objects/host_config/{host_name}`
- **Base URL:** `{apiUrl}`
- **Official documentation:** [Get Host Config](https://docs.checkmk.com/latest/en/rest_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `host_name` | path | `string` | yes | Checkmk host name. |
