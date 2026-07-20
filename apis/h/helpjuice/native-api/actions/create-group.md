# Create Group with Helpjuice

Creates a new group in Helpjuice.

## Endpoint

- **Method:** `POST`
- **Path:** `/groups`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Create Group](https://help.helpjuice.com/api-v3/using-api-v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The Helpjuice group name. |
| `smart_load` | body | `boolean` | no | Whether the group uses smart loading. |
