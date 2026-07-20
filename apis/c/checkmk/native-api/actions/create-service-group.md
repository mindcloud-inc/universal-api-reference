# Create Service Group with Checkmk

Creates a new service group in Checkmk.

## Endpoint

- **Method:** `POST`
- **Path:** `/domain-types/service_group_config/collections/all`
- **Base URL:** `{apiUrl}`
- **Official documentation:** [Create Service Group](https://github.com/Checkmk/checkmk/tree/master/cmk/gui/openapi/endpoints/service_group_config)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Service group name. |
| `alias` | body | `string` | yes | Service group display alias. |
