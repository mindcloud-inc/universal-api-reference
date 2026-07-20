# Update Member with WebWork Time Tracker

Updates an existing member in WebWork Time Tracker.

## Endpoint

- **Method:** `PUT`
- **Path:** `/members/:memberId`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [Update Member](https://api-docs.webwork-tracker.com/api/members/updatemember)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `memberId` | path | `number` | yes |
| `workspace_id` | query | `number` | yes |
| `email` | body | `string` | no |
| `firstname` | body | `string` | no |
| `lastname` | body | `string` | no |
| `timezone` | body | `string` | no |
| `role` | body | `string` | no |
| `rate_status` | body | `number` | no |
| `weekly_hours_limit` | body | `number` | no |
| `remove_avatar` | body | `number` | no |
