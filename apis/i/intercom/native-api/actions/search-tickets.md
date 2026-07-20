# Search Tickets with Intercom

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets/search`
- **Base URL:** `https://api.intercom.io`
- **Official documentation:** [Search Tickets](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/tickets/searchtickets)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `object` | no | — |
| `query.field` | body | `string` | yes | Field to search by |
| `query.operator` | body | `string` | yes | Search operator |
| `query.value` | body | `string` | yes | Value to match |
