# Get YouTube Channel Profile with Transcript Downloader

Retrieves a YouTube channel profile from Transcript Downloader.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/channel/profile`
- **Base URL:** `https://dashboard.transcriptdownloader.com`
- **Official documentation:** [Get YouTube Channel Profile](https://documentation.transcriptdownloader.com/youtube-api#get-profile-information--full-channel-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The YouTube channel URL. |
| `include_webhook` | body | `string` | no | A public webhook URL to receive the completed result. |
