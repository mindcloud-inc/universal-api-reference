# Create Comment with Runrun.it

Creates a new comment in Runrun.it.

## Endpoint

- **Method:** `POST`
- **Path:** `/comments`
- **Base URL:** `https://runrun.it/api/v1.0`
- **Official documentation:** [Create Comment](https://runrun.it/api/documentation#comments-create-a-new-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | body | `number` | yes | Task ID to comment on. |
| `text` | body | `string` | yes | Comment text. |
