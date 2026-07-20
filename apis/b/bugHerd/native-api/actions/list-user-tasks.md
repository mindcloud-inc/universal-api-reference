# List User Tasks with BugHerd

Retrieves tasks for a BugHerd user.

## Endpoint

- **Method:** `GET`
- **Path:** `users/:user_id/tasks.json`
- **Base URL:** `https://www.bugherd.com/api_v2`
- **Official documentation:** [List User Tasks](https://docs.bugherd.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `number` | yes | The BugHerd user ID. |
| `updated_since` | query | `string` | no | Return tasks updated after this timestamp. |
| `created_since` | query | `string` | no | Return tasks created after this timestamp. |
| `priority` | query | `string` | no | Filter tasks by BugHerd priority. |
| `tag` | query | `string` | no | Filter tasks by tag. |
| `assigned_to_id` | query | `number` | no | Filter tasks assigned to a specific user ID. |
