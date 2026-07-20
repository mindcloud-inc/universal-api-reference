# Get a Thread with JustCall

Retrieves a text thread from JustCall.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2.1/texts/threads/:thread_id`
- **Base URL:** `https://api.justcall.io`
- **Official documentation:** [Get a Thread](https://developer.justcall.io/reference/texts_threads_get_v21)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `thread_id` | path | `string` | yes |
| `offset` | query | `number` | no |
| `limit` | query | `number` | no |
