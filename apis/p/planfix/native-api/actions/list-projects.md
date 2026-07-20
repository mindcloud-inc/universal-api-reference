# List Projects with Planfix

Retrieves projects from Planfix.

## Endpoint

- **Method:** `POST`
- **Path:** `/project/list`
- **Base URL:** `{accountBaseUrl}/rest`
- **Official documentation:** [List Projects](https://help.planfix.com/restapidocs/#/Project/get-project-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | body | `string` | no | Comma-delimited project fields to return. |
| `pageSize` | body | `number` | no | Number of projects to return. |
| `offset` | body | `number` | no | Project list offset. |
