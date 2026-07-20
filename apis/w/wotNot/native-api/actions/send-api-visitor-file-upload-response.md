# Send API Visitor File Upload Response with WotNot

Creates an API visitor file upload response in WotNot.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/conversation/:conversation_id/messages`
- **Base URL:** `https://api.wotnot.io`
- **Official documentation:** [Send API Visitor File Upload Response](https://help.wotnot.io/deploy/publishing-agents/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | API-channel conversation ID |
| `message.data.files[0].filename` | body | `string` | yes | Uploaded filename |
| `message.data.files[0].link` | body | `string` | yes | Public URL to the uploaded file |
| `message.data.files[0].mime_type` | body | `string` | yes | Uploaded file MIME type |
| `message.data.files[0].extension` | body | `string` | yes | Uploaded file extension |
