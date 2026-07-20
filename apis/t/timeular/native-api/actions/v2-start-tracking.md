# V2 Start Tracking with Timeular

Creates a tracking session in the Timeular v2 API.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/tracking/:activityId/start`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [V2 Start Tracking](https://developers.early.app/#c82fdaee-4545-4a0b-86c5-dfbaa5b831f2)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `activityId` | path | `string` | yes |
| `startedAt` | body | `string` | no |
