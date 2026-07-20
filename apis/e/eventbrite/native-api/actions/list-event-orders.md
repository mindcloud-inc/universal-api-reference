# List Event Orders with Eventbrite

Retrieves event orders from Eventbrite.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:eventId/orders/`
- **Base URL:** `https://www.eventbriteapi.com/v3`
- **Official documentation:** [List Event Orders](https://www.eventbrite.com/platform/docs/orders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | Event identifier. |
