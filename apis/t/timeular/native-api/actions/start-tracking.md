# Start Tracking with Timeular

Creates a tracking session in your Timeular workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v4/tracking/:activityId/start`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [Start Tracking](https://developers.early.app/#ffc19f68-496d-4a78-9ec1-bd2f21739aee)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `activityId` | path | `string` | yes |
| `startedAt` | body | `string` | no |
