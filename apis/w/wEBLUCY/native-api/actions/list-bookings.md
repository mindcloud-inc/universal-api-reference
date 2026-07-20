# List Bookings with WEBLUCY

Retrieves bookings from WEBLUCY.

## Endpoint

- **Method:** `GET`
- **Path:** `/bookings`
- **Base URL:** `https://apps.weblucy.com/api/site`
- **Official documentation:** [List Bookings](https://websitebuilder.docs.apiary.io/#reference/bookings/list-all-bookings/list-all-bookings)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | query | `string` | no | Filter bookings by event ID. |
| `from` | query | `string` | no | List only bookings created after this Unix timestamp, inclusive. |
| `to` | query | `string` | no | List only bookings created before this Unix timestamp, inclusive. |
