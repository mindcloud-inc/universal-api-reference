# Get Workspace User Capacity Totals with Clockify

Retrieves workspace user capacity totals from Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/scheduling/assignments/user-filter/totals`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Get Workspace User Capacity Totals](https://docs.developer.clockify.me/#tag/Scheduling/operation/getUserTotals)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end` | body | `date` | yes | — |
| `page` | body | `number` | no | — |
| `pageSize` | body | `number` | no | — |
| `search` | body | `string` | no | — |
| `start` | body | `date` | yes | — |
| `statusFilter` | body | `list` | no | Accepted values: `ALL`, `PUBLISHED`, `UNPUBLISHED`. |
| `userFilter` | body | `object` | no | — |
| `userFilter.contains` | body | `list` | no | Accepted values: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `userFilter.ids[]` | body | `array<string>` | no | — |
| `userFilter.sourceType` | body | `list` | no | Accepted values: `USER_GROUP`. |
| `userFilter.status` | body | `list` | no | Accepted values: `ACTIVE`, `ALL`, `DECLINED`, `INACTIVE`, `PENDING`. |
| `userFilter.statuses` | body | `list<string>` | no | Accepted values: `ACTIVE`, `ALL`, `DECLINED`, `INACTIVE`, `PENDING`. Send multiple values as a array. |
| `userFilter.statuses[]` | body | `string` | no | — |
| `userGroupFilter` | body | `object` | no | — |
| `userGroupFilter.contains` | body | `list` | no | Accepted values: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `userGroupFilter.ids[]` | body | `array<string>` | no | — |
| `userGroupFilter.status` | body | `list` | no | Accepted values: `ACTIVE`, `ALL`, `DECLINED`, `INACTIVE`, `PENDING`. |
| `workspaceId` | path | `list<string>` | yes | — |
