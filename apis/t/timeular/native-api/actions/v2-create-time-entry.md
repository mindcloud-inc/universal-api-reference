# V2 Create Time Entry with Timeular

Creates a new time entry in the Timeular v2 API.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/time-entries`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [V2 Create Time Entry](https://developers.early.app/#6e2246f2-bd4b-41a6-a3c9-ac8ab53cadc5)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `activityId` | body | `string` | yes |
| `note` | body | `string` | no |
| `startedAt` | body | `string` | yes |
| `stoppedAt` | body | `string` | yes |
