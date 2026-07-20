# Create Task with Missive

Creates a task in your Missive workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks`
- **Base URL:** `https://public.missiveapp.com/v1`
- **Official documentation:** [Create Task](https://missiveapp.com/docs/developers/rest-api/endpoints#create-a-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Task title. Max 1000 characters. |
| `description` | body | `string` | no | Task description. Max 10000 characters. |
| `state` | body | `list` | no | Task state. Accepted values: `closed`, `in_progress`, `todo`. |
| `organization` | body | `string` | no | Organization ID. Required when using team, assignees, or add_users. |
| `team` | body | `string` | no | Team ID. Either team or assignees is required for standalone tasks. |
| `assignees[]` | body | `array<string>` | no | Array of assignee user IDs. Either team or assignees is required for standalone tasks. |
| `due_at` | body | `date` | no | Unix timestamp for the task due date. |
| `subtask` | body | `boolean` | no | Whether this task is a subtask of a conversation. |
| `conversation` | body | `string` | no | Parent conversation ID. Required when subtask is true. |
| `references[]` | body | `array<string>` | no | Array of references used to find or create the parent conversation. |
| `conversation_subject` | body | `string` | no | Subject for the parent conversation when creating via references. |
| `add_users[]` | body | `array<string>` | no | Array of user IDs to add to the parent conversation. |
| `add_to_inbox` | body | `boolean` | no | Move the parent conversation to Inbox for everyone with access. |
