# Create team membership with Appwrite

Creates a new team membership in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/teams/{teamId}/memberships`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create team membership](https://appwrite.io/docs/references/cloud/server-rest/teams)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roles` | body | `string` | no | Array of strings. Use this param to set the user roles in the team. A role can be any string. Learn more about [roles and permissions](https://appwrite.io/docs/permissions). Maximum of 100 roles are allowed, each 32 characters long. |
| `teamId` | path | `string` | yes | Team ID. |
| `email` | body | `string` | no | Email of the new team member. |
| `userId` | body | `string` | no | ID of the user to be added to a team. |
| `phone` | body | `string` | no | Phone number. Format this number with a leading '+' and a country code, e.g., +16175551212. |
| `roles[]` | body | `array<string>` | yes | Array of strings. Use this param to set the user roles in the team. A role can be any string. Learn more about [roles and permissions](https://appwrite.io/docs/permissions). Maximum of 100 roles are allowed, each 32 characters long. |
| `url` | body | `string` | no | URL to redirect the user back to your app from the invitation email. This parameter is not required when an API key is supplied. Only URLs from hostnames in your project platform list are allowed. This requirement helps to prevent an [open redirect](https://cheatsheetseries.owasp.org/cheatsheets/Unvalidated_Redirects_and_Forwards_Cheat_Sheet.html) attack against your project API. |
| `name` | body | `string` | no | Name of the new team member. Max length: 128 chars. |
