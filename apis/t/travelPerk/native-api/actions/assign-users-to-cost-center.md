# Assign Users to Cost Center with TravelPerk

Assigns users to a cost center in TravelPerk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/cost_centers/:costCenterId/users`
- **Base URL:** `https://api.sandbox-travelperk.com`
- **API:** rest
- **Official documentation:** [Assign Users to Cost Center](https://developers.perk.com/docs/cost-centers-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Api-Version` | `1` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `costCenterId` | path | `string` | yes | The cost center identifier that will receive users. |
| `user_ids[]` | body | `array<string>` | yes | List of user IDs to assign to the cost center. |
