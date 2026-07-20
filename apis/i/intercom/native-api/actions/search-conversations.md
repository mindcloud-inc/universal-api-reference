# Search Conversations with Intercom

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/search`
- **Base URL:** `https://api.intercom.io`
- **Official documentation:** [Search Conversations](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/conversations/searchconversations)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `object` | no | — |
| `query.field` | body | `string` | yes | Field to search by |
| `query.operator` | body | `string` | yes | Search operator |
| `query.value` | body | `string` | yes | Value to match |
