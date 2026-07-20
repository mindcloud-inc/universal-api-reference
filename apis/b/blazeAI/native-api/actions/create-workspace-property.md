# Create Workspace Property with Blaze AI

Creates a workspace property in Blaze AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/w/:workspace_id/properties`
- **Base URL:** `https://api.blaze.ai`
- **Official documentation:** [Create Workspace Property](https://api.blaze.ai/api/documentation#!/properties/postApiV1WWorkspaceIdProperties)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes | — |
| `property[name]` | body | `string` | yes | — |
| `property[type]` | body | `string` | yes | — |
| `property[default_for_articles]` | body | `boolean` | no | — |
| `property[meta][date_format]` | body | `string` | no | — |
| `property[meta][number_format]` | body | `string` | no | — |
| `property[meta][allow_mentioning_multiple_people]` | body | `boolean` | no | — |
| `property[meta][notify_person]` | body | `boolean` | no | — |
| `property[property_values][][value]` | body | `string` | yes | — |
| `property[property_values][][meta][color]` | body | `string` | no | Send multiple values as a array. |
