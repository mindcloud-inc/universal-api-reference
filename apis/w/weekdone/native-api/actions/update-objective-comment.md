# Update Objective Comment with Weekdone

Updates an objective comment in Weekdone.

## Endpoint

- **Method:** `PATCH`
- **Path:** `objective/:objectiveId/comments/:commentId`
- **Base URL:** `https://api.weekdone.com/1/`
- **Official documentation:** [Update Objective Comment](https://weekdone.com/developer#h-objectives)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `commentId` | path | `number` | yes |
| `objectiveId` | path | `number` | yes |
