# Update Activity with Timeular

Updates an existing activity in your Timeular workspace.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v4/activities/:activityId`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [Update Activity](https://developers.early.app/#45a1b847-5182-4fe3-ac01-5a0ac0e811d3)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `activityId` | path | `string` | yes |
| `color` | body | `string` | no |
| `name` | body | `string` | no |
