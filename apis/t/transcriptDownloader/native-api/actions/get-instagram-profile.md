# Get Instagram Profile with Transcript Downloader

Retrieves an Instagram profile from Transcript Downloader.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/instagram/profile`
- **Base URL:** `https://dashboard.transcriptdownloader.com`
- **Official documentation:** [Get Instagram Profile](https://documentation.transcriptdownloader.com/instagram-api#fetch-a-user-profile-process-profile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The Instagram profile URL. |
| `include_webhook` | body | `string` | no | A public webhook URL to receive the completed result. |
