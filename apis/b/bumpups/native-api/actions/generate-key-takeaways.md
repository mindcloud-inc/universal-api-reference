# Generate Key Takeaways with Bumpups

Creates key takeaways from a video in Bumpups.

## Endpoint

- **Method:** `POST`
- **Path:** `/creator/takeaways`
- **Base URL:** `https://api.bumpups.com`
- **Official documentation:** [Generate Key Takeaways](https://docs.bumpups.com/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The YouTube video URL to analyze. |
| `language` | body | `string` | no | The two-letter language code for the response. |
| `emojis_enabled` | body | `boolean` | no | Whether to include emojis in the generated takeaways. |
