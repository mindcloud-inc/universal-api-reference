# Extract Text with ScreenshotAPI

Creates extracted page text in ScreenshotAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/screenshot`
- **Base URL:** `https://shot.screenshotapi.net/v3`
- **Official documentation:** [Extract Text](https://www.screenshotapi.net/docs/renderScreenshot)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | The fully qualified URL to extract text from. |
| `fresh` | query | `boolean` | no | When true, request a newly rendered capture instead of cached output. |
