# List Room Types with Channex

Retrieves room types from your Channex account.

## Endpoint

- **Method:** `GET`
- **Path:** `/room_types`
- **Base URL:** `https://staging.channex.io/api/v1`
- **Official documentation:** [List Room Types](https://docs.channex.io/api-v.1-documentation/room-types-collection#room-types-list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[property_id]` | query | `string` | no | Optional property UUID to narrow the room type list. |
