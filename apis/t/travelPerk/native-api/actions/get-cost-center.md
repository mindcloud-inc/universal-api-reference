# Get Cost Center with TravelPerk

Retrieves a cost center from TravelPerk.

## Endpoint

- **Method:** `GET`
- **Path:** `/cost_centers/:costCenterId`
- **Base URL:** `https://api.sandbox-travelperk.com`
- **API:** rest
- **Official documentation:** [Get Cost Center](https://developers.perk.com/docs/cost-centers-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Api-Version` | `1` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `costCenterId` | path | `string` | yes | The cost center identifier. |
