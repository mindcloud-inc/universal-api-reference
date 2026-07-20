# Create Time Entry with Timeular

Creates a new time entry in your Timeular workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v4/time-entries`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [Create Time Entry](https://developers.early.app/#192b7ce9-d25e-42ff-8c03-b9d06a9b0b75)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `activityId` | body | `string` | yes |
| `note` | body | `string` | no |
| `startedAt` | body | `string` | yes |
| `stoppedAt` | body | `string` | yes |
