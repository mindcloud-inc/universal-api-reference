# List Databases with Gridly

Finds databases in your Gridly workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/databases`
- **Base URL:** `https://api.gridly.com/v1`
- **Official documentation:** [List Databases](https://www.gridly.com/docs/api/#list-databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | query | `number` | no | ID of the project. The ID can be found in the URL of the web application: app.gridly.com/projects/<id>. |
