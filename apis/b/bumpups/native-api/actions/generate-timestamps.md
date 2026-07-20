# Generate Timestamps with Bumpups

Creates timestamps for a video in Bumpups.

## Endpoint

- **Method:** `POST`
- **Path:** `/general/timestamps`
- **Base URL:** `https://api.bumpups.com`
- **Official documentation:** [Generate Timestamps](https://docs.bumpups.com/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The YouTube video URL to analyze. |
| `language` | body | `string` | no | The two-letter language code for the response. |
| `timestamps_style` | body | `string` | no | Preferred length of each timestamp. |
