# Run FFmpeg Command with Rendi

Submits an FFmpeg command for processing in Rendi.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/run-ffmpeg-command`
- **Base URL:** `https://api.rendi.dev`
- **Official documentation:** [Run FFmpeg Command](https://docs.rendi.dev/api-reference/endpoint/run-ffmpeg-command)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ffmpeg_command` | body | `string` | yes | FFmpeg command string with {{in_*}} and {{out_*}} aliases. |
| `input_files` | body | `object` | yes | Object mapping in_* aliases to publicly accessible file URLs. |
| `output_files` | body | `object` | yes | Object mapping out_* aliases to output file names. |
| `max_command_run_seconds` | body | `number` | no | Max runtime for a single FFmpeg command (default 300). |
| `vcpu_count` | body | `number` | no | Number of virtual CPUs to allocate for this command. |
| `metadata` | body | `object` | no | Optional metadata object for tracking/reporting and webhooks. |
| `input_compressed_folder` | body | `string` | no | Public URL to a zip archive with input media files. |
