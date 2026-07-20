# Get Thread with XenForo

Retrieves the specified thread from XenForo.

## Endpoint

- **Method:** `GET`
- **Path:** `/threads/:id/`
- **Base URL:** `{baseUrl}/2310/api`
- **Official documentation:** [Get Thread](https://docs.xenforo.com/api/get-threads-id)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the thread to retrieve. |
| `with_posts` | query | `boolean` | no | If true, include a page of posts with the thread response. |
| `with_first_post` | query | `boolean` | no | If true, include the first post in the thread response. |
| `with_last_post` | query | `boolean` | no | If true, include the last post in the thread response. |
