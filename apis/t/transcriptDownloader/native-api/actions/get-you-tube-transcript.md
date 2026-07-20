# Get YouTube Transcript with Transcript Downloader

Retrieves a YouTube transcript from Transcript Downloader.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/transcripts/:downloadId`
- **Base URL:** `https://dashboard.transcriptdownloader.com`
- **Official documentation:** [Get YouTube Transcript](https://documentation.transcriptdownloader.com/youtube-api#get-a-previously-generated-transcript--metadata-using-download-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `downloadId` | path | `string` | yes | The transcript download ID returned by a create transcript action. |
