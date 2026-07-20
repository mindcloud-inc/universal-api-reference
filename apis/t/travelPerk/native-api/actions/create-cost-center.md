# Create Cost Center with TravelPerk

Creates a new cost center in TravelPerk.

## Endpoint

- **Method:** `POST`
- **Path:** `/cost_centers`
- **Base URL:** `https://api.sandbox-travelperk.com`
- **API:** rest
- **Official documentation:** [Create Cost Center](https://developers.perk.com/docs/cost-centers-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Api-Version` | `1` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the cost center to create. |
