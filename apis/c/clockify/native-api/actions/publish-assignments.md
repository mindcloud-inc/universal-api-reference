# Publish Assignments with Clockify

Publishes workspace scheduling assignments in Clockify.

## Endpoint

- **Method:** `PUT`
- **Path:** `workspaces/:workspaceId/scheduling/assignments/publish`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Publish Assignments](https://docs.developer.clockify.me/#tag/Scheduling/operation/publishAssignments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end` | body | `string` | yes | — |
| `notifyUsers` | body | `boolean` | no | — |
| `search` | body | `string` | no | — |
| `start` | body | `string` | yes | — |
| `userFilter` | body | `object` | no | — |
| `userFilter.contains` | body | `list` | no | Accepted values: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `userFilter.ids[]` | body | `array<string>` | no | — |
| `userFilter.sourceType` | body | `list` | no | Accepted values: `USER_GROUP`. |
| `userFilter.status` | body | `list` | no | Accepted values: `ACTIVE`, `ALL`, `DECLINED`, `INACTIVE`, `PENDING`. |
| `userFilter.statuses` | body | `list<string>` | no | Accepted values: `ACTIVE`, `ALL`, `DECLINED`, `INACTIVE`, `PENDING`. Send multiple values as a array. |
| `userGroupFilter` | body | `object` | no | — |
| `userGroupFilter.contains` | body | `list` | no | Accepted values: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `userGroupFilter.ids[]` | body | `array<string>` | no | — |
| `userGroupFilter.status` | body | `list` | no | Accepted values: `ACTIVE`, `ALL`, `DECLINED`, `INACTIVE`, `PENDING`. |
| `viewType` | body | `list` | no | Accepted values: `ALL`, `PROJECTS`, `TEAM`. |
| `workspaceId` | path | `list<string>` | yes | — |
