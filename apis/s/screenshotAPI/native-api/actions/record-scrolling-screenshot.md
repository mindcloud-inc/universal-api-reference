# Record Scrolling Screenshot with ScreenshotAPI

Creates a scrolling screenshot recording in ScreenshotAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/screenshot`
- **Base URL:** `https://shot.screenshotapi.net/v3`
- **Official documentation:** [Record Scrolling Screenshot](https://www.screenshotapi.net/docs/scrollingScreenshot)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | The fully qualified URL to record as a scrolling screenshot. |
| `file_type` | query | `string` | no | The scrolling capture file format. |
| `scroll_speed` | query | `string` | no | Control how quickly the page scrolls during capture. |
| `duration` | query | `number` | no | Capture duration in seconds for the scrolling recording. |
| `scroll_back` | query | `boolean` | no | Scroll back to the top after reaching the bottom of the page. |
| `start_immediately` | query | `boolean` | no | Begin recording immediately without waiting for page load. |
| `fresh` | query | `boolean` | no | Request a newly rendered scrolling capture instead of cached output. |
