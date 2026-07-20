# Create YouTube Transcript with Transcript Downloader

Creates a YouTube transcript in Transcript Downloader.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/transcripts`
- **Base URL:** `https://dashboard.transcriptdownloader.com`
- **Official documentation:** [Create YouTube Transcript](https://documentation.transcriptdownloader.com/youtube-api#initialize-transcription--metadata-using-youtube-video-id-and-language)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `youtube_video_id` | body | `string` | yes | The YouTube video ID to transcribe. |
| `language` | body | `string` | yes | The transcript language code, such as en or de. |
| `include_comments` | body | `boolean` | no | Whether to include video comments in the response. |
| `include_webhook` | body | `string` | no | A public webhook URL to receive the completed result. |
