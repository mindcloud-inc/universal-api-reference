# Create Or Update Team with Sales Cookie

Creates or updates a team in Sales Cookie by name.

## Endpoint

- **Method:** `POST`
- **Path:** `/Api/SetTeam`
- **Base URL:** `https://salescookie.com/app`
- **Official documentation:** [Create Or Update Team](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-programmatically-create-or-update-teams)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Team name used to create or update the team. |
| `description` | body | `string` | no | — |
| `managerId` | body | `string` | no | Optional system user ID for the team manager. |
| `parentTeamId` | body | `string` | no | Optional parent team ID. |
| `managerCanViewResults` | body | `boolean` | no | — |
| `managerCanViewCredits` | body | `boolean` | no | — |
| `membersCanViewCredits` | body | `boolean` | no | — |
