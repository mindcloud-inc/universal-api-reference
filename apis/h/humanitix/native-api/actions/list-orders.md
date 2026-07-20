# List Orders with Humanitix

Retrieves orders for an event from Humanitix.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:eventId/orders`
- **Base URL:** `https://api.humanitix.com/v1`
- **Official documentation:** [List Orders](https://humanitix.stoplight.io/docs/humanitix-public-api/468f50b741494-get-orders)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | The Humanitix event ID. |
