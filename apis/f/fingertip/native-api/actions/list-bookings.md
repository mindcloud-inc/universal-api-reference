# List Bookings with Fingertip

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/bookings`
- **Base URL:** `https://api.fingertip.com`
- **Official documentation:** [List Bookings](https://docs.fingertip.com/openapi-specs/list-bookings.md)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | query | `string` | yes | ID of the site to list bookings for. |
| `status` | query | `string` | no | Optional booking status filter. |
