# Get Host Group with Checkmk

Retrieves host group details from Checkmk.

## Endpoint

- **Method:** `GET`
- **Path:** `/objects/host_group_config/{name}`
- **Base URL:** `{apiUrl}`
- **Official documentation:** [Get Host Group](https://github.com/Checkmk/checkmk/tree/master/cmk/gui/openapi/endpoints/host_group_config)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Host group name. |
