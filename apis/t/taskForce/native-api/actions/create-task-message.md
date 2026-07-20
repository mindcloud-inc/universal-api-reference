# Create Task Message with TaskForce

Sends a task message in TaskForce.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/:taskId/messages`
- **Base URL:** `https://www.task-force.app/api`
- **Official documentation:** [Create Task Message](https://task-force.app/skill.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Message text. |
| `taskId` | path | `string` | yes | Task identifier. |
