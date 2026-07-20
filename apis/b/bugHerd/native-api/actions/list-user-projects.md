# List User Projects with BugHerd

Retrieves projects for a BugHerd user.

## Endpoint

- **Method:** `GET`
- **Path:** `users/:user_id/projects.json`
- **Base URL:** `https://www.bugherd.com/api_v2`
- **Official documentation:** [List User Projects](https://docs.bugherd.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `number` | yes | The BugHerd user ID. |
| `created_since` | query | `string` | no | Return projects created after this timestamp. |
| `is_active` | query | `boolean` | no | Filter by active status. |
