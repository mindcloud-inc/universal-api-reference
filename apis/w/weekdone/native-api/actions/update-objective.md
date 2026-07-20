# Update Objective with Weekdone

Updates an existing objective in Weekdone.

## Endpoint

- **Method:** `PATCH`
- **Path:** `objective/:objectiveId`
- **Base URL:** `https://api.weekdone.com/1/`
- **Official documentation:** [Update Objective](https://weekdone.com/developer#h-objectives)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `description` | body | `string` | yes |
| `objectiveId` | path | `number` | yes |
