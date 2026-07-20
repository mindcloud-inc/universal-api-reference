# Initialize YouTube Audio Download with Transcript Downloader

Creates a YouTube audio download in Transcript Downloader.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/downloads/audio`
- **Base URL:** `https://dashboard.transcriptdownloader.com`
- **Official documentation:** [Initialize YouTube Audio Download](https://documentation.transcriptdownloader.com/youtube-api#initialize-a-download-process-audio)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `youtube_video_id` | body | `string` | yes | The YouTube video ID to process. |
| `include_webhook` | body | `string` | no | A public webhook URL to receive the completed result. |
