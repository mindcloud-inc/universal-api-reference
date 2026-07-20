# V2 Stop Tracking with Timeular

Creates a time entry by stopping tracking in the Timeular v2 API.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/tracking/:trackingId/stop`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [V2 Stop Tracking](https://developers.early.app/#311094a8-3290-4735-be03-96953dc3d44b)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `stoppedAt` | body | `string` | no |
| `trackingId` | path | `string` | yes |
