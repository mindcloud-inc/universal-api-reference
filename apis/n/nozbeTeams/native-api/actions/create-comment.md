# Create Comment with Nozbe Teams

Creates a new comment in Nozbe Teams.

## Endpoint

- **Method:** `POST`
- **Path:** `/comments`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [Create Comment](https://api4.nozbe.com/v1/api#/comments/postComment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | yes | The comment text. |
| `task_id` | body | `string` | yes | The task that will receive the comment. |
