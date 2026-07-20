# Get Forum Threads with XenForo

Retrieves a page of forum threads from XenForo.

## Endpoint

- **Method:** `GET`
- **Path:** `/forums/:id/threads`
- **Base URL:** `{baseUrl}/2310/api`
- **Official documentation:** [Get Forum Threads](https://docs.xenforo.com/api/get-forums-id-threads)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the forum whose threads should be returned. |
| `unread` | query | `boolean` | no | Filters to unread threads only. Ignored for guests. |
