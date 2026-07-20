# Initialize Instagram Audio Download with Transcript Downloader

Creates an Instagram audio download in Transcript Downloader.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/instagram/audio`
- **Base URL:** `https://dashboard.transcriptdownloader.com`
- **Official documentation:** [Initialize Instagram Audio Download](https://documentation.transcriptdownloader.com/instagram-api#initialize-instagram-audio-download-process-audio)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The Instagram post or reel URL. |
| `include_webhook` | body | `string` | no | A public webhook URL to receive the completed result. |
