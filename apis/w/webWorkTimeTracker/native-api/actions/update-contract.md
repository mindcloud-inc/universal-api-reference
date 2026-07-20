# Update Contract with WebWork Time Tracker

Updates an existing contract in WebWork Time Tracker.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contracts/:contractId`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [Update Contract](https://api-docs.webwork-tracker.com/api/contracts/updatecontract)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contractId` | path | `number` | yes |
| `workspace_id` | query | `number` | yes |
| `weekly_hours_limit` | body | `number` | no |
| `screenshots` | body | `string` | no |
| `rate` | body | `number` | no |
| `status` | body | `string` | no |
