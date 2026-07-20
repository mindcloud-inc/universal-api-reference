# Update SCIM User with TravelPerk

Updates an existing SCIM user in TravelPerk.

## Endpoint

- **Method:** `PUT`
- **Path:** `https://app.sandbox-travelperk.com/api/v2/scim/Users/:scimUserId`
- **Base URL:** `https://api.sandbox-travelperk.com`
- **API:** rest
- **Official documentation:** [Update SCIM User](https://developers.perk.com/docs/using-the-scim-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/scim+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scimUserId` | path | `string` | yes | The SCIM user identifier to update. |
| `name.givenName` | body | `string` | yes | The user's given name. |
| `name.familyName` | body | `string` | yes | The user's family name. |
| `userName` | body | `string` | yes | The work email address used as the SCIM username. |
| `active` | body | `boolean` | no | Whether the user should be active in TravelPerk. |
