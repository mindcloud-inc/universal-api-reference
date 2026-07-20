# Create Time Off Request with Clockify

Creates a time off request in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/time-off/policies/:policyId/requests`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Create Time Off Request](https://docs.developer.clockify.me/#tag/Time-Off/operation/createTimeOffRequest)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `policyId` | path | `string<string>` | yes |
| `timeOffPeriod` | body | `object` | yes |
| `note` | body | `string` | no |
| `timeOffPeriod.halfDayPeriod` | body | `string` | no |
| `timeOffPeriod.isHalfDay` | body | `boolean` | no |
| `timeOffPeriod.period` | body | `object` | yes |
| `timeOffPeriod.period.days` | body | `number` | no |
| `timeOffPeriod.period.end` | body | `string` | no |
| `timeOffPeriod.period.start` | body | `string` | no |
| `timeOffPeriod.timeOffHalfDayPeriod` | body | `string` | no |
