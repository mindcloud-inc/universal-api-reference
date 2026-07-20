# Get Listing Daily Pricing with FleetWire

Retrieves listing daily pricing from FleetWire.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/listings/:l_id/daily_pricing`
- **Base URL:** `https://api.fleetwire.io`
- **Official documentation:** [Get Listing Daily Pricing](https://documenter.getpostman.com/view/263138/Tz5p6dWS)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end` | query | `string` | no | End datetime for daily pricing. |
| `l_id` | path | `string` | no | The FleetWire listing identifier. |
| `start` | query | `string` | no | Start datetime for daily pricing. |
