# Update membership with Appwrite

Updates the membership in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/teams/{teamId}/memberships/{membershipId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update membership](https://appwrite.io/docs/references/cloud/server-rest/teams)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roles` | body | `string` | no | An array of strings. Use this param to set the user's roles in the team. A role can be any string. Learn more about [roles and permissions](https://appwrite.io/docs/permissions). Maximum of 100 roles are allowed, each 32 characters long. |
| `teamId` | path | `string` | yes | Team ID. |
| `membershipId` | path | `string` | yes | Membership ID. |
| `roles[]` | body | `array<string>` | yes | An array of strings. Use this param to set the user's roles in the team. A role can be any string. Learn more about [roles and permissions](https://appwrite.io/docs/permissions). Maximum of 100 roles are allowed, each 32 characters long. |
