# List Tag Tasks with GoodDay.work

Finds tasks with a specific GoodDay.work tag.

## Endpoint

- **Method:** `GET`
- **Path:** `/tag/:tagId/tasks`
- **Base URL:** `https://api.goodday.work/2.0`
- **Official documentation:** [List Tag Tasks](https://www.goodday.work/developers/api-v2/projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tagId` | path | `string` | yes | GoodDay tag ID. |
| `closed` | query | `boolean` | no | Include closed tasks. |
