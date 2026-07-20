# Get Member with WebWork Time Tracker

Retrieves a member from WebWork Time Tracker.

## Endpoint

- **Method:** `GET`
- **Path:** `/members/:memberId`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [Get Member](https://api-docs.webwork-tracker.com/api/members/getmember)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `memberId` | path | `number` | yes |
| `workspace_id` | query | `number` | yes |
