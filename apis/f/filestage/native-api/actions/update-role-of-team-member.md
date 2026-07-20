# Update Role of Team Member with Filestage

Updates a team member role in Filestage.

## Endpoint

- **Method:** `PUT`
- **Path:** `/team/members/{memberId}/role`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Update Role of Team Member](https://developers.filestage.io/docs/api/ilqk7tdu1swil-update-role-of-team-member)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `memberId` | path | `string` | yes | Filestage user id |
| `roleId` | body | `string` | yes | The ID of the role from the `Get Team Roles` endpoint. |
