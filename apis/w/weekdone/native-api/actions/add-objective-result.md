# Add Objective Result with Weekdone

Creates a key result for an objective in Weekdone.

## Endpoint

- **Method:** `POST`
- **Path:** `objective/:objectiveId/result`
- **Base URL:** `https://api.weekdone.com/1/`
- **Official documentation:** [Add Objective Result](https://weekdone.com/developer#h-key-results)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `description` | body | `string` | yes |
| `objectiveId` | path | `number` | yes |
