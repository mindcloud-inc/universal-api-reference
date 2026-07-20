# List Comments with Nozbe Teams

Retrieves accessible comments from Nozbe Teams.

## Endpoint

- **Method:** `GET`
- **Path:** `/comments`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [List Comments](https://api4.nozbe.com/v1/api#/comments/getComments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | query | `string` | no | Return only comments for this task. |
