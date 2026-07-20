# Render Screenshot JSON with ScreenshotAPI

Creates screenshot metadata in ScreenshotAPI with selectable file output.

## Endpoint

- **Method:** `GET`
- **Path:** `/screenshot`
- **Base URL:** `https://shot.screenshotapi.net/v3`
- **Official documentation:** [Render Screenshot JSON](https://www.screenshotapi.net/docs/renderScreenshot)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | The fully qualified URL to capture. |
| `file_type` | query | `string` | no | The screenshot file format to generate. |
| `fresh` | query | `boolean` | no | When true, request a newly rendered screenshot instead of cached output. |
