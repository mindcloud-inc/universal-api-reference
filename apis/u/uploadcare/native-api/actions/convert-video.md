# Convert Video with Uploadcare

Creates a video conversion in Uploadcare.

## Endpoint

- **Method:** `POST`
- **Path:** `/convert/video/`
- **Base URL:** `https://api.uploadcare.com`
- **Official documentation:** [Convert Video](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/Conversion/operation/videoConvert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `paths[]` | body | `array<string>` | yes | List of source video paths to convert. |
| `store` | body | `string` | no | Whether to store converted video outputs permanently. |
