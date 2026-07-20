# Render Screenshot with ScreenshotAPI

Creates a new PNG screenshot in ScreenshotAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/screenshot`
- **Base URL:** `https://shot.screenshotapi.net/v3`
- **Official documentation:** [Render Screenshot](https://www.screenshotapi.net/docs/renderScreenshot)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | The fully qualified URL to capture. |
| `fresh` | query | `boolean` | no | When true, request a newly rendered screenshot instead of cached output. |
