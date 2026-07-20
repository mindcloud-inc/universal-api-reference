# Complete task with comment with OkoCRM

Marks a task as done in OkoCRM with a comment.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/done/[:id]`
- **Base URL:** `https://api.okocrm.com/v2`
- **Official documentation:** [Complete task with comment](https://okocrm.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The OkoCRM task ID. |
| `text` | body | `string` | no | Comment to leave when completing the task. |
