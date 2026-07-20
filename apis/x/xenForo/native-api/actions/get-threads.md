# Get Threads with XenForo

Retrieves a list of threads from XenForo.

## Endpoint

- **Method:** `GET`
- **Path:** `/threads/`
- **Base URL:** `{baseUrl}/2310/api`
- **Official documentation:** [Get Threads](https://docs.xenforo.com/api/get-threads)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `unread` | query | `boolean` | no | Filters to unread threads only. Ignored for guests. |
| `last_days` | query | `number` | no | Filters to threads that have had a reply in the last X days. |
