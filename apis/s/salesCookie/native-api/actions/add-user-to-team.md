# Add User To Team with Sales Cookie

Adds a user to a team in Sales Cookie.

## Endpoint

- **Method:** `POST`
- **Path:** `/Api/CreateTeamMember`
- **Base URL:** `https://salescookie.com/app`
- **Official documentation:** [Add User To Team](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-programmatically-add-or-remove-users-from-teams)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `systemUserId` | body | `string` | yes | System user ID of the user to add. |
| `teamId` | body | `string` | yes | Team ID to add the user to. |
