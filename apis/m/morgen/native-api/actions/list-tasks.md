# List Tasks with Morgen

Retrieves tasks from Morgen.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/tasks/list`
- **Base URL:** `https://api.morgen.so`
- **Official documentation:** [List Tasks](https://docs.morgen.so/tasks#list-tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum tasks to return, up to 100. |
| `updatedAfter` | query | `string` | no | Only return tasks updated after this ISO 8601 datetime. |
