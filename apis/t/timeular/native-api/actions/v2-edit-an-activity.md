# V2 Edit an Activity with Timeular

Updates an existing activity in the Timeular v2 API.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/activities/:activityId`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [V2 Edit an Activity](https://developers.early.app/#e89a59c1-1151-4c52-b1e9-3b9f7f5492b7)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `activityId` | path | `string` | yes |
| `color` | body | `string` | no |
| `name` | body | `string` | no |
