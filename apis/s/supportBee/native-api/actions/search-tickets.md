# Search Tickets with SupportBee

Finds tickets in SupportBee by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/tickets/search`
- **Base URL:** `https://{company}.supportbee.com`
- **Official documentation:** [Search Tickets](https://supportbee.com/docs/api/reference#tag/Tickets/paths/~1tickets~1search/get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Search query string. |
| `spam` | query | `boolean` | no | If true, include spam tickets. |
| `trash` | query | `boolean` | no | If true, include trashed tickets. |
