# Update Cost Center with TravelPerk

Updates an existing cost center in TravelPerk.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/cost_centers/:costCenterId`
- **Base URL:** `https://api.sandbox-travelperk.com`
- **API:** rest
- **Official documentation:** [Update Cost Center](https://developers.perk.com/docs/cost-centers-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Api-Version` | `1` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `costCenterId` | path | `string` | yes | The cost center identifier to update. |
| `name` | body | `string` | no | Updated name for the cost center. |
