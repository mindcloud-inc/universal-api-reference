# Get Events By Collection with OpenSea

Retrieves events for an OpenSea collection.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/events/collection/{slug}`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Get Events By Collection](https://docs.opensea.io/reference/list_events_by_collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | Unique identifier for the collection |
| `after` | query | `number` | no | Only show events after this timestamp (Unix timestamp in seconds) |
| `before` | query | `number` | no | Only show events before this timestamp (Unix timestamp in seconds) |
| `event_type[]` | query | `array<string>` | no | Filter by event types. To get order invalidation and revalidation events, please use the Stream API. The order status can also be checked on the Get Order endpoint. Send multiple values as a string separated by `,`. |
| `limit` | query | `number` | no | Number of items to return per page |
| `next.value` | query | `string` | no | — |
