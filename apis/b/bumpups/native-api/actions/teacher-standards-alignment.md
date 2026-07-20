# Teacher Standards Alignment with Bumpups

Creates standards alignment from a video in Bumpups.

## Endpoint

- **Method:** `POST`
- **Path:** `/chat`
- **Base URL:** `https://api.bumpups.com`
- **Official documentation:** [Teacher Standards Alignment](https://docs.bumpups.com/docs/prompt-cookbook/teacher)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The YouTube video URL to analyze. |
| `language` | body | `string` | no | The two-letter language code for the response. |
| `output_format` | body | `string` | no | The desired output format. |
