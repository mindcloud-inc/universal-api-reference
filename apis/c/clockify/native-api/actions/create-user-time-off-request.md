# Create User Time Off Request with Clockify

Creates a time off request for a user in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/time-off/policies/:policyId/users/:userId/requests`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Create User Time Off Request](https://docs.developer.clockify.me/#tag/Time-Off/operation/createTimeOffRequestForOther)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `policyId` | path | `string<string>` | yes |
| `userId` | path | `string<string>` | yes |
| `timeOffPeriod` | body | `object` | yes |
| `note` | body | `string` | no |
| `timeOffPeriod.halfDayPeriod` | body | `string` | no |
| `timeOffPeriod.isHalfDay` | body | `boolean` | no |
| `timeOffPeriod.period` | body | `object` | yes |
| `timeOffPeriod.period.days` | body | `number` | no |
| `timeOffPeriod.period.end` | body | `string` | no |
| `timeOffPeriod.period.start` | body | `string` | no |
| `timeOffPeriod.timeOffHalfDayPeriod` | body | `string` | no |
