# Create Host Group with Checkmk

Creates a new host group in Checkmk.

## Endpoint

- **Method:** `POST`
- **Path:** `/domain-types/host_group_config/collections/all`
- **Base URL:** `{apiUrl}`
- **Official documentation:** [Create Host Group](https://github.com/Checkmk/checkmk/tree/master/cmk/gui/openapi/endpoints/host_group_config)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Host group name. |
| `alias` | body | `string` | yes | Host group display alias. |
