# Get SCIM User with TravelPerk

Retrieves a SCIM user from TravelPerk.

## Endpoint

- **Method:** `GET`
- **Path:** `https://app.sandbox-travelperk.com/api/v2/scim/Users/:scimUserId`
- **Base URL:** `https://api.sandbox-travelperk.com`
- **API:** rest
- **Official documentation:** [Get SCIM User](https://developers.perk.com/docs/using-the-scim-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/scim+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scimUserId` | path | `string` | yes | The SCIM user identifier. |
