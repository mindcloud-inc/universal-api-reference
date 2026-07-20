# V2 Edit Tracking with Timeular

Updates the current tracking session in the Timeular v2 API.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/tracking/:trackingId`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [V2 Edit Tracking](https://developers.early.app/#623e655f-a6e0-43b6-8c2a-6e7fcccaa4dd)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `note` | body | `string` | no |
| `trackingId` | path | `string` | yes |
