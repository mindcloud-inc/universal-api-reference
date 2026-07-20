# Generate Video Description with Bumpups

Creates a video description in Bumpups.

## Endpoint

- **Method:** `POST`
- **Path:** `/creator/description`
- **Base URL:** `https://api.bumpups.com`
- **Official documentation:** [Generate Video Description](https://docs.bumpups.com/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The YouTube video URL to analyze. |
| `language` | body | `string` | no | The two-letter language code for the response. |
