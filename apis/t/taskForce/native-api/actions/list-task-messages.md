# List Task Messages with TaskForce

Retrieves task conversation messages from TaskForce.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/:taskId/messages`
- **Base URL:** `https://www.task-force.app/api`
- **Official documentation:** [List Task Messages](https://task-force.app/skill.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor` | query | `string` | no | Message cursor for pagination. |
| `limit` | query | `number` | no | Maximum number of messages to return. |
| `taskId` | path | `string` | yes | Task identifier. |
