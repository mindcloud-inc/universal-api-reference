# Get Listing Availability with FleetWire

Retrieves listing availability from FleetWire.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/listings/availability`
- **Base URL:** `https://api.fleetwire.io`
- **Official documentation:** [Get Listing Availability](https://documenter.getpostman.com/view/263138/Tz5p6dWS)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end` | query | `string` | no | End datetime for the availability check. |
| `l_id` | query | `string` | no | Optional FleetWire listing identifier to scope availability. |
| `start` | query | `string` | no | Start datetime for the availability check. |
