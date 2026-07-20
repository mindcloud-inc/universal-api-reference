# Student Real-World Application with Bumpups

Creates real-world application ideas from a video in Bumpups.

## Endpoint

- **Method:** `POST`
- **Path:** `/chat`
- **Base URL:** `https://api.bumpups.com`
- **Official documentation:** [Student Real-World Application](https://docs.bumpups.com/docs/prompt-cookbook/student)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The YouTube video URL to analyze. |
| `language` | body | `string` | no | The two-letter language code for the response. |
| `output_format` | body | `string` | no | The desired output format. |
