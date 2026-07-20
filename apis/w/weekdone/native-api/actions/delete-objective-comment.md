# Delete Objective Comment with Weekdone

Deletes a comment from an objective in Weekdone.

## Endpoint

- **Method:** `DELETE`
- **Path:** `objective/:objectiveId/comments/:commentId`
- **Base URL:** `https://api.weekdone.com/1/`
- **Official documentation:** [Delete Objective Comment](https://weekdone.com/developer#h-objectives)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `commentId` | path | `number` | yes |
| `objectiveId` | path | `number` | yes |
