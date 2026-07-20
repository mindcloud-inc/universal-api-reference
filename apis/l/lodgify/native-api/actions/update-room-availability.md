# Update Room Availability with Lodgify

Updates a room's availability in Lodgify.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/availability/:propertyId/:roomTypeId/set`
- **Base URL:** `https://api.lodgify.com`
- **Official documentation:** [Update Room Availability](https://docs.lodgify.com/reference/post_v1-availability-propertyid-roomtypeid-set)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `propertyId` | path | `number` | yes |
| `roomTypeId` | path | `number` | yes |
