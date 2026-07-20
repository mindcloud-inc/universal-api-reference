# Upload File with Recut URL Shortener

Uploads a file to Recut URL Shortener.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/upload/:filename`
- **Base URL:** `https://app.recut.in/api`
- **Official documentation:** [Upload File](https://app.recut.in/developers#upload-a-file)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | path | `string` | yes | File name including extension to place in the upload URL |
| `fileData` | body | `file` | yes | Binary file data to send as the raw request body |
| `name` | query | `string` | no | Display name for the uploaded file |
| `custom` | query | `string` | no | Custom alias instead of random alias |
| `domain` | query | `string` | no | Custom domain |
| `password` | query | `string` | no | Password protection |
| `expiry` | query | `date` | no | Expiration date such as 2021-09-28 |
| `maxdownloads` | query | `number` | no | Maximum number of downloads |
