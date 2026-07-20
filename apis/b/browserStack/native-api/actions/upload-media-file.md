# Upload Media File with BrowserStack

Uploads a media file to BrowserStack Automate.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api-cloud.browserstack.com/automate/upload-media`
- **Base URL:** `https://api.browserstack.com`
- **Official documentation:** [Upload Media File](https://www.browserstack.com/docs/automate/api-reference/selenium/media#upload-media-file)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Public URL or base64 content for the media file to upload. |
