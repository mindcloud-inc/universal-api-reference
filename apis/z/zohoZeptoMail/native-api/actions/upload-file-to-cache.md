# Upload File to Cache with Zoho ZeptoMail

Uploads a file to the Zoho ZeptoMail cache.

## Endpoint

- **Method:** `POST`
- **Path:** `files`
- **Base URL:** `https://api.zeptomail.com/v1.1`
- **Official documentation:** [Upload File to Cache](https://www.zoho.com/zeptomail/help/api/file-upload.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | yes | Name of the file being uploaded to ZeptoMail file cache. |
| `data` | body | `string` | yes | Binary or text payload to upload to file cache. |
