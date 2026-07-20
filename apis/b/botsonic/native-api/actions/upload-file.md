# Upload File with Botsonic

Uploads a file as bot data in Botsonic.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/business/bot-data/upload-file`
- **Base URL:** `https://api.botsonic.ai`
- **Official documentation:** [Upload File](https://docs.botsonic.com/reference/upload_file_v1_business_bot_data_upload_file_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Upload identifier. |
| `bot_id` | body | `string` | yes | Bot identifier. |
| `file_url` | body | `string` | yes | URL of the file to upload. |
| `file_name` | body | `string` | no | Optional file name. |
