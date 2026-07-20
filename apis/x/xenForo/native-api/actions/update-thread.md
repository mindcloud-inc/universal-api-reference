# Update Thread with XenForo

Updates an existing thread in XenForo.

## Endpoint

- **Method:** `POST`
- **Path:** `/threads/:id/`
- **Base URL:** `{baseUrl}/2310/api`
- **Official documentation:** [Update Thread](https://docs.xenforo.com/api/post-threads-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the thread to update. |
| `title` | body | `string` | no | New thread title. |
| `discussion_open` | body | `boolean` | no | Whether the thread should be open for replies. |
| `sticky` | body | `boolean` | no | Whether the thread should be sticky. |
