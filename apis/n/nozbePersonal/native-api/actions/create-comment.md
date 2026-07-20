# Create Comment with Nozbe Personal

Creates a new comment in Nozbe Personal.

## Endpoint

- **Method:** `POST`
- **Path:** `/comments`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [Create Comment](https://api4.nozbe.com/v1/api#/comments/postComment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | yes | Comment body text. |
| `task_id` | body | `string` | yes | Task ID for the comment. |
