# Update Objective Result with Weekdone

Updates a key result for an objective in Weekdone.

## Endpoint

- **Method:** `PATCH`
- **Path:** `objective/:objectiveId/result/:resultId`
- **Base URL:** `https://api.weekdone.com/1/`
- **Official documentation:** [Update Objective Result](https://weekdone.com/developer#h-key-results)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `description` | body | `string` | no |
| `objectiveId` | path | `number` | yes |
| `progress` | body | `number` | no |
| `resultId` | path | `number` | yes |
