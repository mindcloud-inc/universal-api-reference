# List Trips with TravelPerk

Retrieves trips from TravelPerk.

## Endpoint

- **Method:** `GET`
- **Path:** `/trips`
- **Base URL:** `https://api.sandbox-travelperk.com`
- **API:** rest
- **Official documentation:** [List Trips](https://developers.perk.com/docs/rest-api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Api-Version` | `1` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `traveler_id` | query | `string` | no | Filter trips by the traveler identifier. |
