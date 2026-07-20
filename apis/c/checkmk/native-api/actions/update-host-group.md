# Update Host Group with Checkmk

Updates an existing host group in Checkmk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/objects/host_group_config/{name}`
- **Base URL:** `{apiUrl}`
- **Official documentation:** [Update Host Group](https://github.com/Checkmk/checkmk/tree/master/cmk/gui/openapi/endpoints/host_group_config)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Host group name. |
| `alias` | body | `string` | yes | Updated host group alias. |
