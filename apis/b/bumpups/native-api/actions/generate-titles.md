# Generate Titles with Bumpups

Creates title suggestions for a video in Bumpups.

## Endpoint

- **Method:** `POST`
- **Path:** `/creator/titles`
- **Base URL:** `https://api.bumpups.com`
- **Official documentation:** [Generate Titles](https://docs.bumpups.com/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The YouTube video URL to analyze. |
| `language` | body | `string` | no | The two-letter language code for the response. |
