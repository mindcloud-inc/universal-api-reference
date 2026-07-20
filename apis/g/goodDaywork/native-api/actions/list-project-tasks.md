# List Project Tasks with GoodDay.work

Finds tasks in a GoodDay.work project.

## Endpoint

- **Method:** `GET`
- **Path:** `/project/:projectId/tasks`
- **Base URL:** `https://api.goodday.work/2.0`
- **Official documentation:** [List Project Tasks](https://www.goodday.work/developers/api-v2/projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | GoodDay project ID. |
| `closed` | query | `boolean` | no | Include closed tasks. |
| `subfolders` | query | `boolean` | no | Include tasks from subfolders. |
