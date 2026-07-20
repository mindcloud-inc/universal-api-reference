# List All Threads with JustCall

Retrieves text threads from JustCall.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2.1/texts/threads`
- **Base URL:** `https://api.justcall.io`
- **Official documentation:** [List All Threads](https://developer.justcall.io/reference/texts_threads_list_v21)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `phone_id` | query | `number` | yes |
| `from_datetime` | query | `string` | no |
| `to_datetime` | query | `string` | no |
| `contact_number` | query | `string` | no |
| `keyword` | query | `string` | no |
| `tag_id` | query | `number` | no |
| `order` | query | `string` | no |
