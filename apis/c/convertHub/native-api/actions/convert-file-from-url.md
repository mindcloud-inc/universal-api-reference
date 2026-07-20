# Convert File from URL with ConvertHub

Creates a file conversion job from a URL in ConvertHub.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/convert-url`
- **Base URL:** `https://api.converthub.com/v2`
- **Official documentation:** [Convert File from URL](https://converthub.com/api/docs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_url` | body | `string` | yes | URL of the file to convert (must be HTTP/HTTPS) |
| `target_format` | body | `string` | yes | Target format extension (e.g., "pdf", "jpg", "mp3") |
| `output_filename` | body | `string` | no | Custom name for the output file |
| `webhook_url` | body | `string` | no | URL to receive webhook notification when complete |
| `options` | body | `object` | no | Format-specific conversion options |
| `options.quality` | body | `number` | no | Quality setting (1-100) for lossy formats |
| `options.resolution` | body | `string` | no | Resolution for image/video conversions |
| `options.bitrate` | body | `string` | no | Bitrate for audio/video conversions |
| `options.sample_rate` | body | `number` | no | Sample rate for audio conversions |
| `metadata` | body | `object` | no | Custom metadata for tracking |
