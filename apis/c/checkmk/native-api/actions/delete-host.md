# Delete Host with Checkmk

Deletes an existing host from Checkmk.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/objects/host_config/{host_name}`
- **Base URL:** `{apiUrl}`
- **Official documentation:** [Delete Host](https://docs.checkmk.com/latest/en/rest_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `host_name` | path | `string` | yes | Checkmk host name to delete. |
