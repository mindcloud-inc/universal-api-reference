# Upload Text with Botsonic

Uploads text as bot data in Botsonic.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/business/bot-data/upload-text`
- **Base URL:** `https://api.botsonic.ai`
- **Official documentation:** [Upload Text](https://docs.botsonic.com/reference/upload_text_v1_business_bot_data_upload_text_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Upload identifier. |
| `bot_id` | body | `string` | yes | Bot identifier. |
| `title` | body | `string` | no | Optional title for the uploaded text. |
| `text` | body | `string` | yes | Training text to upload. |
