# Get Instagram Content with Transcript Downloader

Retrieves Instagram content metadata from Transcript Downloader.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/instagram/content`
- **Base URL:** `https://dashboard.transcriptdownloader.com`
- **Official documentation:** [Get Instagram Content](https://documentation.transcriptdownloader.com/instagram-api#fetch-content-metadata-using-the-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The Instagram post or reel URL. |
| `include_webhook` | body | `string` | no | A public webhook URL to receive the completed result. |
