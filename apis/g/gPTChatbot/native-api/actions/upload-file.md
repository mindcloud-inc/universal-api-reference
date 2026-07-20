# Upload File with GPT Chatbot

Uploads a file as a source for a chatbot in GPT Chatbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/chatbot/:uuid/data-source/upload`
- **Base URL:** `https://app.gptchatbot.it/api/v1`
- **Official documentation:** [Upload File](https://docs.gptchatbot.it/api-reference/data-sources/create-file)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | Chatbot uuid. |
| `filePath` | body | `file` | yes | File uploaded as multipart form-data. |
| `reference_source_link` | body | `string` | no | Reference source link for the uploaded file. |
