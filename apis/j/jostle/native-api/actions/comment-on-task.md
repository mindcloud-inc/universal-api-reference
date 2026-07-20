# Comment on Task with Jostle

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/tasks/task/:id/comment`
- **Base URL:** `https://api-prod.jostle.us`
- **Official documentation:** [Comment on Task](https://api.jostle.me/reference/commenttask-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Id for the targeted task |
| `commentText` | body | `string` | yes | Comment text up to 2500 characters |
