# Add User with HubSpot

Creates a new user in HubSpot.

## Endpoint

- **Method:** `POST`
- **Path:** `settings/v3/users/`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Add User](https://developers.hubspot.com/docs/api-reference/settings-user-provisioning-v3/users/post-settings-v3-users-)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address for the new HubSpot user. |
| `sendWelcomeEmail` | body | `boolean` | yes | Whether HubSpot should email the user a welcome message. |
| `firstName` | body | `string` | no | First name for the user. |
| `lastName` | body | `string` | no | Last name for the user. |
| `primaryTeamId` | body | `string` | no | Primary HubSpot team ID for the user. |
| `roleId` | body | `string` | no | HubSpot role ID to assign to the user. |
| `secondaryTeamIds[]` | body | `array<string>` | no | Additional HubSpot team IDs for the user. |
