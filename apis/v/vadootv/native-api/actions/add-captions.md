# Add captions with Vadootv

Creates a captioned video in Vadootv.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/add_captions`
- **Base URL:** `https://aiapi.vadoo.tv`
- **Official documentation:** [Add captions](https://docs.vadoo.tv/docs/guide/create-ai-captions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the video to caption. |
| `language` | body | `string` | no | Language of the source video. |
| `theme` | body | `string` | no | Caption theme name. |
