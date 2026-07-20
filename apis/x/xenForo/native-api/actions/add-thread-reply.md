# Add Thread Reply with XenForo

Creates a reply post in XenForo.

## Endpoint

- **Method:** `POST`
- **Path:** `/posts/`
- **Base URL:** `{baseUrl}/2310/api`
- **Official documentation:** [Add Thread Reply](https://docs.xenforo.com/api/post-posts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `thread_id` | body | `number` | yes | ID of the thread to reply to. |
| `message` | body | `string` | yes | Reply message body. |
