# Delete Host Group with Checkmk

Deletes an existing host group from Checkmk.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/objects/host_group_config/{name}`
- **Base URL:** `{apiUrl}`
- **Official documentation:** [Delete Host Group](https://github.com/Checkmk/checkmk/tree/master/cmk/gui/openapi/endpoints/host_group_config)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Host group name. |
