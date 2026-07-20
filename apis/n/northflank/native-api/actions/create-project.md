# Create project with Northflank

Creates a new project in Northflank.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://api.northflank.com/v1`
- **Official documentation:** [Create project](https://northflank.com/docs/v1/api/use-the-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the project. |
| `region` | body | `string` | no | The region the project will be hosted in. |
