# Delete Objective Result with Weekdone

Deletes a key result from an objective in Weekdone.

## Endpoint

- **Method:** `DELETE`
- **Path:** `objective/:objectiveId/result/:resultId`
- **Base URL:** `https://api.weekdone.com/1/`
- **Official documentation:** [Delete Objective Result](https://weekdone.com/developer#h-key-results)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `objectiveId` | path | `number` | yes |
| `resultId` | path | `number` | yes |
