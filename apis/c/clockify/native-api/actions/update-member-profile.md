# Update Member Profile with Clockify

Updates a member profile in Clockify.

## Endpoint

- **Method:** `PATCH`
- **Path:** `workspaces/:workspaceId/member-profile/:userId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update Member Profile](https://docs.developer.clockify.me/#tag/User/operation/updateMemberProfileWithAdditionalData)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `userId` | path | `string<string>` | yes | — |
| `imageUrl` | body | `string` | no | — |
| `name` | body | `string` | no | Maximum length: 100. |
| `removeProfileImage` | body | `boolean` | no | — |
| `userCustomFields[]` | body | `array<object>` | no | — |
| `weekStart` | body | `list<string>` | no | Accepted values: `FRIDAY`, `MONDAY`, `SATURDAY`, `SUNDAY`, `THURSDAY`, `TUESDAY`, `WEDNESDAY`. |
| `workCapacity` | body | `string` | no | — |
| `workingDays` | body | `list<string>` | no | Accepted values: `FRIDAY`, `MONDAY`, `SATURDAY`, `SUNDAY`, `THURSDAY`, `TUESDAY`, `WEDNESDAY`. |
| `userCustomFields[].customFieldId` | body | `string` | yes | — |
| `userCustomFields[].value` | body | `object` | no | — |
