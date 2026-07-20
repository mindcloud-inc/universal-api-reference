# Translate video with Fliz

Creates a translated video in Fliz.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/rest/videos/:from_video_id/translate`
- **Base URL:** `https://app.fliz.ai`
- **Official documentation:** [Translate video](https://app.fliz.ai/api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_video_id` | path | `string` | yes | The UUID of the existing video to translate. |
| `new_lang` | body | `string` | yes | Target two-character ISO 639-1 language code. |
| `is_automatic` | body | `boolean` | no | Whether the translated video will be generated to the end automatically. |
| `webhook_url` | body | `string` | no | Webhook URL called when rendering completes or errors. |
