# Update Project Memberships with Clockify

Updates workspace project memberships in Clockify.

## Endpoint

- **Method:** `PATCH`
- **Path:** `workspaces/:workspaceId/projects/:projectId/memberships`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update Project Memberships](https://docs.developer.clockify.me/#tag/Project/operation/updateMemberships)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `projectId` | path | `string<string>` | yes |
| `memberships[]` | body | `array<object>` | yes |
| `userGroups` | body | `object` | no |
| `memberships[].costRate` | body | `object` | no |
| `memberships[].costRate.amount` | body | `number` | yes |
| `memberships[].costRate.since` | body | `string` | no |
| `memberships[].hourlyRate` | body | `object` | no |
| `memberships[].hourlyRate.amount` | body | `number` | yes |
| `memberships[].hourlyRate.since` | body | `string` | no |
| `memberships[].userId` | body | `string` | yes |
| `userGroups.contains` | body | `string` | no |
| `userGroups.ids[]` | body | `array<string>` | no |
| `userGroups.status` | body | `string` | no |
