# Convert Audio to MP3 with Cloudmersive Video and Media

Converts an audio file to MP3 in Cloudmersive Video and Media.

## Endpoint

- **Method:** `POST`
- **Path:** `/video/convert/to/mp3`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Convert Audio to MP3](https://api.cloudmersive.com/docs/video.asp#operation--video-convert-to-mp3-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileUrl` | body | `string` | no | URL of an audio file to convert. Cloudmersive recommends this option for files larger than 2GB. |
| `inputFile` | body | `file` | no | Input audio file to convert. |
| `bitRate` | body | `number` | no | Desired bitrate in kilobytes per second (48 to 1411). |
