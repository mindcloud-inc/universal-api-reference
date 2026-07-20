# Archive Member with WebWork Time Tracker

Archives a member in WebWork Time Tracker.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/members/:memberId`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [Archive Member](https://api-docs.webwork-tracker.com/api/members/deletemember)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `memberId` | path | `number` | yes |
| `workspace_id` | query | `number` | yes |
