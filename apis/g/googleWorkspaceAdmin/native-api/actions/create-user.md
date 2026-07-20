# Create User with Google Workspace Admin

Creates a new user in Google Workspace Admin.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/directory/v1/users`
- **Base URL:** `https://admin.googleapis.com`
- **Official documentation:** [Create User](https://developers.google.com/workspace/admin/directory/reference/rest/v1/users/insert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `primaryEmail` | body | `string` | yes | The user's primary email address. Must be unique and cannot be an alias of another user. |
| `password` | body | `string` | yes | ASCII password between 8 and 100 characters. |
| `name.givenName` | body | `string` | yes | The user's given name. |
| `name.familyName` | body | `string` | yes | The user's family name. |
| `changePasswordAtNextLogin` | body | `boolean` | no | Whether the user must change their password the next time they sign in. |
| `orgUnitPath` | body | `string` | no | Optional organizational unit path for the new user. |
