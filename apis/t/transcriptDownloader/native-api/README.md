# Transcript Downloader: Native API Reference

A consolidated summary of Transcript Downloader's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://documentation.transcriptdownloader.com/api-documentation
- **API base URL:** `https://dashboard.transcriptdownloader.com`

## Authentication

### API Key

Connect with a Transcript Downloader API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://documentation.transcriptdownloader.com/api-documentation#authorization)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,503`. Wait 1 ms before the first retry. Stop after 5 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Transcript with Speaker Labels](actions/create-transcript-with-speaker-labels.md) | `POST /api/transcriptspeakerid` | [docs](https://documentation.transcriptdownloader.com/youtube-api#create-transcript-with-speaker-labels) |
| [Create YouTube Transcript](actions/create-you-tube-transcript.md) | `POST /api/transcripts` | [docs](https://documentation.transcriptdownloader.com/youtube-api#initialize-transcription--metadata-using-youtube-video-id-and-language) |
| [Get Download](actions/get-download.md) | `GET /downloads/:downloadId` | [docs](https://documentation.transcriptdownloader.com/youtube-api#get-a-download-direct-url-link-to-download) |
| [Get Instagram Content](actions/get-instagram-content.md) | `POST /api/instagram/content` | [docs](https://documentation.transcriptdownloader.com/instagram-api#fetch-content-metadata-using-the-url) |
| [Get Instagram Profile](actions/get-instagram-profile.md) | `POST /api/instagram/profile` | [docs](https://documentation.transcriptdownloader.com/instagram-api#fetch-a-user-profile-process-profile) |
| [Get YouTube Channel Profile](actions/get-you-tube-channel-profile.md) | `POST /api/channel/profile` | [docs](https://documentation.transcriptdownloader.com/youtube-api#get-profile-information--full-channel-list) |
| [Get YouTube Transcript](actions/get-you-tube-transcript.md) | `GET /api/transcripts/:downloadId` | [docs](https://documentation.transcriptdownloader.com/youtube-api#get-a-previously-generated-transcript--metadata-using-download-id) |
| [Initialize Instagram Audio Download](actions/initialize-instagram-audio-download.md) | `POST /api/instagram/audio` | [docs](https://documentation.transcriptdownloader.com/instagram-api#initialize-instagram-audio-download-process-audio) |
| [Initialize YouTube Audio Download](actions/initialize-you-tube-audio-download.md) | `POST /api/downloads/audio` | [docs](https://documentation.transcriptdownloader.com/youtube-api#initialize-a-download-process-audio) |
| [List Instagram Posts and Reels](actions/list-instagram-posts-and-reels.md) | `POST /api/instagram/list` | [docs](https://documentation.transcriptdownloader.com/instagram-api#get-all-posts--reels-list-of-the-profile) |
| [Test Webhook URL](actions/test-webhook-url.md) | `POST /api/webhook/test` | [docs](https://documentation.transcriptdownloader.com/webhooks#1-test-your-webhook-url) |
