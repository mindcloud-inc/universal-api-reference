# Create Transcript with Speaker Labels with Transcript Downloader

Creates a transcript with speaker labels in Transcript Downloader.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/transcriptspeakerid`
- **Base URL:** `https://dashboard.transcriptdownloader.com`
- **Official documentation:** [Create Transcript with Speaker Labels](https://documentation.transcriptdownloader.com/youtube-api#create-transcript-with-speaker-labels)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transcript_with_speaker_id` | body | `string` | yes | The transcript_speaker_id returned from an audio download response. |
| `include_webhook` | body | `string` | no | A public webhook URL to receive the completed result. |
