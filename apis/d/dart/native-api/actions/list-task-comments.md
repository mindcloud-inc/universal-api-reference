# List Task Comments with Dart

Retrieves task comments from Dart with pagination.

## Endpoint

- **Method:** `GET`
- **Path:** `/comments/list`
- **Base URL:** `https://app.dartai.com/api/v0/public`
- **Official documentation:** [List Task Comments](https://app.dartai.com/api/v0/public/docs/#/Comment/listComments)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `limit` | query | `string` | no |
| `offset` | query | `string` | no |
| `task_id` | query | `string` | no |
