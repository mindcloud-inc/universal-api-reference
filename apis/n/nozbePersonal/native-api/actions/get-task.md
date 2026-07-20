# Get Task with Nozbe Personal

Retrieves a task from Nozbe Personal by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/:id`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [Get Task](https://api4.nozbe.com/v1/api#/tasks/getTaskById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Task ID to retrieve. |
| `fields` | query | `string` | no | Comma-separated list of fields to return. |
