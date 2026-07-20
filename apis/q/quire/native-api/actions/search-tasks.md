# Search Tasks with Quire

Finds tasks in a Quire project by search text.

## Endpoint

- **Method:** `GET`
- **Path:** `task/search/id/:projectId`
- **Base URL:** `https://quire.io/api`
- **Official documentation:** [Search Tasks](https://quire.io/dev/api/#operation--task-search-id--projectId--get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The project ID or shortcut, for example App_Account. |
| `text` | query | `string` | no | Task title text to search for within the project. |
