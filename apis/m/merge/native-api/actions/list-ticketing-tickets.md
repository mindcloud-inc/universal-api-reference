# List Ticketing Tickets with Merge

## Endpoint

- **Method:** `GET`
- **Path:** `/api/ticketing/v1/tickets`
- **Base URL:** `https://api.merge.dev`
- **Official documentation:** [List Ticketing Tickets](https://docs.merge.dev/ticketing/tickets/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountToken` | query | `string` | yes | Linked account token for the Merge account you want to query. The shared headers mapper sends this input as X-Account-Token. |
