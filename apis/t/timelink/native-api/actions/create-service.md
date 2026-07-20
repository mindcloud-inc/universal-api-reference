# Create Service with Timelink

Creates a service in the Timelink workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/services`
- **Base URL:** `https://api.timelink.io/api/v1`
- **Official documentation:** [Create Service](https://api.timelink.io/documentation#/Services/post_api_v1_services)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `ext_tool_id` | body | `string` | no |
