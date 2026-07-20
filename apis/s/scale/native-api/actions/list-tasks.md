# List Tasks with Scale

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/tasks`
- **Base URL:** `https://api.scale.com`
- **Official documentation:** [List Tasks](https://docs.genai.scale.com/v2/tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batch_id` | query | `string` | no | Optional batch identifier filter. |
| `batch_name` | query | `string` | no | Optional batch name filter. |
| `completed_after` | query | `string` | no | Only return tasks completed after this timestamp. |
| `completed_before` | query | `string` | no | Only return tasks completed before this timestamp. |
| `expand` | query | `string` | no | Comma-separated fields to expand in the response. |
| `fields` | query | `string` | no | Comma-separated properties to include in the task response. |
| `limit` | query | `string` | no | Limit the number of tasks returned. |
| `page_token` | query | `string` | no | Pagination token for the next page. |
| `project_id` | query | `string` | yes | Scale project identifier. Required in MindCloud for this action. |
| `project_name` | query | `string` | no | Optional alternative to Project ID when you want to scope by project name instead. |
| `status` | query | `string` | no | Optional task status filter. |
