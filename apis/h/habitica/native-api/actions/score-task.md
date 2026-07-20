# Score Task with Habitica

Scores a task in Habitica.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/:taskId/score/:direction`
- **Base URL:** `https://habitica.com/api/v3`
- **Official documentation:** [Score Task](https://habitica.com/apidoc/#api-Task-ScoreTask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The Habitica task ID. |
| `direction` | path | `string` | yes | Score direction, usually up or down. Accepted values: `0`, `1`. |
