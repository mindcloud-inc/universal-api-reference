# Get Events with OpenSea

Retrieves events from OpenSea.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/events`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Get Events](https://docs.opensea.io/reference/list_events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `number` | no | Only show events after this timestamp (Unix timestamp in seconds) |
| `before` | query | `number` | no | Only show events before this timestamp (Unix timestamp in seconds) |
| `event_type[]` | query | `array<string>` | no | Filter by event types. To get order invalidation and revalidation events, please use the Stream API. The order status can also be checked on the Get Order endpoint. Send multiple values as a string separated by `,`. |
| `limit` | query | `number` | no | Number of items to return per page |
| `next.value` | query | `string` | no | — |
