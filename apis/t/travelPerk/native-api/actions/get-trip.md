# Get Trip with TravelPerk

Retrieves a trip from TravelPerk.

## Endpoint

- **Method:** `GET`
- **Path:** `/trips/:tripId`
- **Base URL:** `https://api.sandbox-travelperk.com`
- **API:** rest
- **Official documentation:** [Get Trip](https://developers.perk.com/docs/rest-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Api-Version` | `1` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tripId` | path | `string` | yes | The TravelPerk trip identifier. |
