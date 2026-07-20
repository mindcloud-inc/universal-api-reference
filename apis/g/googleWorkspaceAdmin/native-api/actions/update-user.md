# Update User with Google Workspace Admin

Updates an existing user in Google Workspace Admin.

## Endpoint

- **Method:** `PUT`
- **Path:** `/admin/directory/v1/users/:userKey`
- **Base URL:** `https://admin.googleapis.com`
- **Official documentation:** [Update User](https://developers.google.com/workspace/admin/directory/reference/rest/v1/users/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userKey` | path | `string` | yes | User primary email, alias, or unique ID. |
| `name.givenName` | body | `string` | no | Updated given name for the user. |
| `name.familyName` | body | `string` | no | Updated family name for the user. |
| `suspended` | body | `boolean` | no | Whether the user is suspended. |
| `changePasswordAtNextLogin` | body | `boolean` | no | Whether the user must change their password the next time they sign in. |
| `orgUnitPath` | body | `string` | no | Updated organizational unit path for the user. |
