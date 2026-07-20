# Create Video Item with Google Forms

Creates a video item in Google Forms.

## Endpoint

- **Method:** `POST`
- **Path:** `/:formId:batchUpdate`
- **Base URL:** `https://forms.googleapis.com/v1/forms`
- **Official documentation:** [Create Video Item](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form identifier. |
| `title` | body | `string` | no | Optional item title. |
| `youtubeUri` | body | `string` | yes | YouTube URI for the video. |
| `caption` | body | `string` | no | Text displayed below the video. |
| `alignment` | body | `list` | no | How to align the video in the form. Accepted values: `0`, `1`, `2`. |
| `width` | body | `number` | no | Video width in pixels. |
| `locationIndex` | body | `number` | yes | Where to place the new video item in the form. |
