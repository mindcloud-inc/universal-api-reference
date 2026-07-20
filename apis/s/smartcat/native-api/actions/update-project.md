# Update Project with Smartcat

Updates an existing project in Smartcat.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/integration/v1/project/:projectId`
- **Base URL:** `https://smartcat.ai`
- **Official documentation:** [Update Project](https://developers.smartcat.com/api/#update-a-project-by-id)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Smartcat project ID |
| `name` | body | `string` | no | Updated Smartcat project name. |
| `deadline` | body | `string` | no | Updated project deadline in ISO 8601 format. |
