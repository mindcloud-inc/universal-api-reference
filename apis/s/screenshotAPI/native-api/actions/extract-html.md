# Extract HTML with ScreenshotAPI

Creates extracted page HTML in ScreenshotAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/screenshot`
- **Base URL:** `https://shot.screenshotapi.net/v3`
- **Official documentation:** [Extract HTML](https://www.screenshotapi.net/docs/renderScreenshot)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | The fully qualified URL to extract HTML from. |
| `fresh` | query | `boolean` | no | When true, request a newly rendered capture instead of cached output. |
