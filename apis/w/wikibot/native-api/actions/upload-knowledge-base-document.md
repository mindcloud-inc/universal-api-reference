# Upload Knowledge Base Document with Wikibot

Uploads a knowledge base document to Wikibot.

## Endpoint

- **Method:** `POST`
- **Path:** `/bot/kb/upload-file`
- **Base URL:** `https://api.wikibot.pro/api`
- **Official documentation:** [Upload Knowledge Base Document](https://wikibot.pro/docs/api/kb-upload)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | PDF or DOCX file to upload to the knowledge base. |
