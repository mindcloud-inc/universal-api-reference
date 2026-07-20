# Create Thread with XenForo

Creates a new thread in XenForo.

## Endpoint

- **Method:** `POST`
- **Path:** `/threads/`
- **Base URL:** `{baseUrl}/2310/api`
- **Official documentation:** [Create Thread](https://docs.xenforo.com/api/post-threads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `node_id` | body | `number` | yes | ID of the forum to create the thread in. |
| `title` | body | `string` | yes | Title of the thread. |
| `message` | body | `string` | yes | Body of the first post in the thread. |
