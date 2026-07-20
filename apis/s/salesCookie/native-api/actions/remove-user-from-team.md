# Remove User From Team with Sales Cookie

Removes a user from a team in Sales Cookie.

## Endpoint

- **Method:** `POST`
- **Path:** `/Api/DeleteTeamMember`
- **Base URL:** `https://salescookie.com/app`
- **Official documentation:** [Remove User From Team](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-programmatically-add-or-remove-users-from-teams)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `systemUserId` | body | `string` | yes | System user ID of the user to remove. |
| `teamId` | body | `string` | yes | Team ID to remove the user from. |
