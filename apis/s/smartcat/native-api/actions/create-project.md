# Create Project with Smartcat

Creates a new project in Smartcat.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/integration/v1/project/create`
- **Base URL:** `https://smartcat.ai`
- **Official documentation:** [Create Project](https://developers.smartcat.com/api/#create-the-project)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `REQUEST` | body | `object` | yes | JSON object describing the project to create. |
