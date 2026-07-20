# Record Multiple Scrolling Screenshots with ScreenshotAPI

Creates multiple scrolling screenshot recordings in ScreenshotAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/screenshot`
- **Base URL:** `https://shot.screenshotapi.net/v3`
- **Official documentation:** [Record Multiple Scrolling Screenshots](https://www.screenshotapi.net/docs/scrollingScreenshot)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | The fully qualified URL to record at multiple target sizes. |
| `file_type` | query | `string` | no | The scrolling capture file format. |
| `sizes` | query | `string` | yes | JSON array string describing the output sizes to generate. |
| `fresh` | query | `boolean` | no | Request a newly rendered scrolling capture instead of cached output. |
