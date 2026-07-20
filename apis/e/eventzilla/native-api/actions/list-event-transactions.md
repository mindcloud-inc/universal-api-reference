# List Event Transactions with Eventzilla

Retrieves transactions for an event from Eventzilla.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:eventid/transactions`
- **Base URL:** `https://www.eventzillaapi.net/api/v2`
- **Official documentation:** [List Event Transactions](https://developer.eventzilla.net/docs/#ev_transactions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventid` | path | `number` | yes | The Eventzilla event identifier. |
