# Update Activity with EARLY

Updates an activity in EARLY.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v4/activities/:activityId`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [Update Activity](https://developers.early.app/#45a1b847-5182-4fe3-ac01-5a0ac0e811d3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activityId` | path | `string` | yes | Activity ID. |
| `name` | body | `string` | no | Updated activity name. |
| `color` | body | `string` | no | Updated activity color in hex format. |
