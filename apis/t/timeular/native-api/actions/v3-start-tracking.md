# V3 Start Tracking with Timeular

Creates a tracking session in the Timeular v3 API.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/tracking/:activityId/start`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [V3 Start Tracking](https://developers.early.app/#4d1dcf30-125a-48d3-8895-27e611581f50)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `activityId` | path | `string` | yes |
| `startedAt` | body | `string` | no |
