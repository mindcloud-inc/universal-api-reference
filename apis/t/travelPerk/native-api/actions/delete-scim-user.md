# Delete SCIM User with TravelPerk

Deletes an existing SCIM user from TravelPerk.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://app.sandbox-travelperk.com/api/v2/scim/Users/:scimUserId`
- **Base URL:** `https://api.sandbox-travelperk.com`
- **API:** rest
- **Official documentation:** [Delete SCIM User](https://developers.perk.com/docs/using-the-scim-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/scim+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scimUserId` | path | `string` | yes | The SCIM user identifier to delete. |
