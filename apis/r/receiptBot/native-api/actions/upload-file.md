# Upload File with Receipt Bot

Uploads a base64-encoded file to Receipt Bot.

## Endpoint

- **Method:** `POST`
- **Path:** `/FileUpload`
- **Base URL:** `https://api.receipt-bot.com`
- **Official documentation:** [Upload File](https://documenter.getpostman.com/view/14388213/2sA3kYjLPj)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `moduleId` | body | `number` | no | Receipt Bot module identifier. |
| `fileName` | body | `string` | yes | File name including extension. |
| `fileContent` | body | `string` | yes | Base64-encoded file content. |
| `documentTypeId` | body | `number` | no | Receipt Bot document type identifier. |
