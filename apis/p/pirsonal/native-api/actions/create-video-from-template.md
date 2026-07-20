# Create Video From Template with Pirsonal

Creates a new video from a Pirsonal template.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `https://app.pirsonal.com`
- **Official documentation:** [Create Video From Template](https://app.pirsonal.com/docAPI#Template_Video_New)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateID` | body | `string` | yes | Template ID used to generate the video. |
| `video` | body | `object` | yes | Video_t object with input media, variables, output, and metadata. |
