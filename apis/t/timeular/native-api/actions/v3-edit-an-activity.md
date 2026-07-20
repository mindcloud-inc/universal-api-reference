# V3 Edit an Activity with Timeular

Updates an existing activity in the Timeular v3 API.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v3/activities/:activityId`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [V3 Edit an Activity](https://developers.early.app/#1ac62610-1bb7-411c-846b-c9690fa3ace5)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `activityId` | path | `string` | yes |
| `color` | body | `string` | no |
| `name` | body | `string` | no |
