# Generate PDF with ScreenshotAPI

Creates a new PDF capture in ScreenshotAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/screenshot`
- **Base URL:** `https://shot.screenshotapi.net/v3`
- **Official documentation:** [Generate PDF](https://www.screenshotapi.net/docs/renderScreenshot)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | The fully qualified URL to render as a PDF. |
| `fresh` | query | `boolean` | no | When true, request a newly rendered PDF instead of cached output. |
