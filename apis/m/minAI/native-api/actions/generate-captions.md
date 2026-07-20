# Generate captions with 1minAI

Creates captions and transcripts for video in 1minAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/features`
- **Base URL:** `https://api.1min.ai`
- **Official documentation:** [Generate captions](https://docs.1min.ai/docs/api/ai-for-video/caption-generator/caption-generator-tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `videoUrl` | body | `string` | yes | — |
| `language` | body | `string` | no | — |
| `responseFormat` | body | `list` | no | Accepted values: `JSON`, `SRT`, `Text`, `VTT`, `Verbose JSON`. |
| `timestampGranularities` | body | `string` | no | — |
