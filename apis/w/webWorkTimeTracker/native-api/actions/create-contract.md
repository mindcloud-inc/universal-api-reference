# Create Contract with WebWork Time Tracker

Creates a new contract in WebWork Time Tracker.

## Endpoint

- **Method:** `POST`
- **Path:** `/contracts`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [Create Contract](https://api-docs.webwork-tracker.com/api/contracts/createcontract)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | query | `number` | yes |
| `project_id` | body | `number` | yes |
| `user_id` | body | `number` | yes |
| `weekly_hours_limit` | body | `number` | no |
| `screenshots` | body | `string` | no |
| `rate` | body | `number` | no |
