# <img src="https://images.mindcloud.co/apps/icons/images-5_1774375260302.png" alt="Transcript Downloader logo" width="28" height="28"> Transcript Downloader: Universal API

Extract transcripts, audio, and profile metadata from YouTube and Instagram

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/transcriptDownloader/latest
- **Category:** Marketing / Social Media
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://transcriptdownloader.com
- **Vendor API docs:** https://documentation.transcriptdownloader.com/api-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get YouTube Channel Profile](actions/get-you-tube-channel-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/get-you-tube-channel-profile?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [Get YouTube Channel Profile](actions/get-you-tube-channel-profile.md) | GET | Retrieves a YouTube channel profile from Transcript Downloader. |

### Download

| Action | Method | Description |
| --- | --- | --- |
| [Get Download](actions/get-download.md) | GET | Retrieves a download from Transcript Downloader. |
| [Initialize Instagram Audio Download](actions/initialize-instagram-audio-download.md) | POST | Creates an Instagram audio download in Transcript Downloader. |
| [Initialize YouTube Audio Download](actions/initialize-you-tube-audio-download.md) | POST | Creates a YouTube audio download in Transcript Downloader. |

### Instagram Content

| Action | Method | Description |
| --- | --- | --- |
| [Get Instagram Content](actions/get-instagram-content.md) | GET | Retrieves Instagram content metadata from Transcript Downloader. |
| [List Instagram Posts and Reels](actions/list-instagram-posts-and-reels.md) | GET | Retrieves Instagram posts and reels from Transcript Downloader. |

### Instagram Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Instagram Profile](actions/get-instagram-profile.md) | GET | Retrieves an Instagram profile from Transcript Downloader. |

### Speaker Transcript

| Action | Method | Description |
| --- | --- | --- |
| [Create Transcript with Speaker Labels](actions/create-transcript-with-speaker-labels.md) | POST | Creates a transcript with speaker labels in Transcript Downloader. |

### Transcript

| Action | Method | Description |
| --- | --- | --- |
| [Create YouTube Transcript](actions/create-you-tube-transcript.md) | POST | Creates a YouTube transcript in Transcript Downloader. |
| [Get YouTube Transcript](actions/get-you-tube-transcript.md) | GET | Retrieves a YouTube transcript from Transcript Downloader. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Test Webhook URL](actions/test-webhook-url.md) | POST | Tests a webhook URL in Transcript Downloader. |

