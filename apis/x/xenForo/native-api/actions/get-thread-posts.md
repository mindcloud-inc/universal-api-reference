# Get Thread Posts with XenForo

Retrieves posts from a thread in XenForo.

## Endpoint

- **Method:** `GET`
- **Path:** `/threads/:id/posts`
- **Base URL:** `{baseUrl}/2310/api`
- **Official documentation:** [Get Thread Posts](https://docs.xenforo.com/api/get-threads-id-posts)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the thread whose posts should be returned. |
