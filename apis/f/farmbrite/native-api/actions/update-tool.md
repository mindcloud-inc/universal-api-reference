# Update tool with Farmbrite

Updates an existing tool in Farmbrite.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tools/:tool_id`
- **Base URL:** `https://api.farmbrite.com/v1`
- **Official documentation:** [Update tool](https://developers.farmbrite.com/docs/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `tool_id` | path | `string` | yes |
| `description` | body | `string` | no |
