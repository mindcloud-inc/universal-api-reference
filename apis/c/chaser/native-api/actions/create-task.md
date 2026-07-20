# Create Task with Chaser

Creates a new task in Chaser.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/tasks`
- **Base URL:** `https://slack.chaseforme.com`
- **Official documentation:** [Create Task](https://www.trychaser.com/incoming-webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `summary` | body | `string` | yes | Task summary text. |
| `assignee` | body | `string` | no | Assignee email address or Slack user group handle. Multiple assignees can be comma-separated. |
| `dueAt` | body | `date` | no | Due date in YYYY-MM-DD format. |
| `dueTime` | body | `string` | no | Optional due time in HH:mm format using the task creator timezone. |
| `channel` | body | `string` | no | Optional Slack channel name. Omit to create the task in the creator's direct-message context. |
| `multiAssignStrategy` | body | `string` | no | Optional strategy for multiple assignees: volunteer or round_robin. Accepted values: `0`, `1`, `2`. |
