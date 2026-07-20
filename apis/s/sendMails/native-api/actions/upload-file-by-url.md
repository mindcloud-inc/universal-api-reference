# Upload File By Url with SendMails

Uploads a file to SendMails from a URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/file/upload`
- **Base URL:** `https://app.sendmails.io/api/v1`
- **Official documentation:** [Upload File By Url](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#7-toc-title)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `files` | query | `string` | yes | JSON array string of file objects, each with a required url and optional subdirectory, as documented by SendMails. |
