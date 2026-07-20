# Get Upload with Strava

Retrieves an activity upload from Strava.

## Endpoint

- **Method:** `GET`
- **Path:** `/uploads/:uploadId`
- **Base URL:** `https://www.strava.com/api/v3`
- **Official documentation:** [Get Upload](https://developers.strava.com/docs/reference/#api-Uploads-getUploadById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uploadId` | path | `string` | yes | The identifier of the upload. |
