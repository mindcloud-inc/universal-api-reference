# Get Download with Transcript Downloader

Retrieves a download from Transcript Downloader.

## Endpoint

- **Method:** `GET`
- **Path:** `/downloads/:downloadId`
- **Base URL:** `https://dashboard.transcriptdownloader.com`
- **Official documentation:** [Get Download](https://documentation.transcriptdownloader.com/youtube-api#get-a-download-direct-url-link-to-download)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `downloadId` | path | `string` | yes | The download ID returned by a Transcript Downloader create action. |
