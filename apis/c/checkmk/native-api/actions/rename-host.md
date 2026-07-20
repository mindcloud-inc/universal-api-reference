# Rename Host with Checkmk

Renames an existing host in Checkmk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/objects/host_config/{host_name}/actions/rename/invoke`
- **Base URL:** `{apiUrl}`
- **Official documentation:** [Rename Host](https://docs.checkmk.com/latest/en/rest_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `host_name` | path | `string` | yes | Current Checkmk host name. |
| `new_name` | body | `string` | yes | New Checkmk host name. |
