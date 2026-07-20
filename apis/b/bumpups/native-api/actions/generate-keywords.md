# Generate Keywords with Bumpups

Creates keywords for a video in Bumpups.

## Endpoint

- **Method:** `POST`
- **Path:** `/creator/hashtags`
- **Base URL:** `https://api.bumpups.com`
- **Official documentation:** [Generate Keywords](https://docs.bumpups.com/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The YouTube video URL to analyze. |
| `language` | body | `string` | no | The two-letter language code for the response. |
