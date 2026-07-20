# Deposition Follow-Up Questions with Bumpups

Creates deposition follow-up questions in Bumpups.

## Endpoint

- **Method:** `POST`
- **Path:** `/chat`
- **Base URL:** `https://api.bumpups.com`
- **Official documentation:** [Deposition Follow-Up Questions](https://docs.bumpups.com/docs/prompt-cookbook/legal)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The YouTube video URL to analyze. |
| `language` | body | `string` | no | The two-letter language code for the response. |
| `output_format` | body | `string` | no | The desired output format. |
