# Create Project with Queue

Creates a new project in Queue.

## Endpoint

- **Method:** `POST`
- **Path:** `projects`
- **Base URL:** `https://app.usequeue.com/api/v1`
- **Official documentation:** [Create Project](https://docs.usequeue.com/api-reference/projects/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | query | `string` | no | Title of the project. Must be a string and usually the name of your client. For example AirBnB. |
| `avatar` | query | `string` | no | — |
| `private` | query | `boolean` | no | — |
| `archive` | query | `boolean` | no | — |
