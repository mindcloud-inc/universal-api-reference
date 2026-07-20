# Create Client with Timelink

Creates a client in the Timelink workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/clients`
- **Base URL:** `https://api.timelink.io/api/v1`
- **Official documentation:** [Create Client](https://api.timelink.io/documentation#/Clients/post_api_v1_clients)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `ext_tool_id` | body | `string` | no |
