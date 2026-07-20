# <img src="https://images.mindcloud.co/apps/icons/eranol_1775054999192.png" alt="Eranol logo" width="28" height="28"> Eranol: Universal API

Create, edit, and convert videos and audio with Eranol

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eranol/latest
- **Category:** Communication / Video Communications
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.eranol.com/
- **Vendor API docs:** https://www.eranol.com/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify API Key](actions/verify-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eranol/latest/actions/verify-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Account Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify API Key](actions/verify-api-key.md) | GET | Verifies whether your Eranol API key is valid. |

### Media Job

| Action | Method | Description |
| --- | --- | --- |
| [Add Background Audio](actions/add-background-audio.md) | POST | Creates a background audio job in Eranol. |
| [Add Intro](actions/add-intro.md) | POST | Creates an intro addition job in Eranol. |
| [Add Outro](actions/add-outro.md) | POST | Creates an outro addition job in Eranol. |
| [Convert Audio To MP3](actions/convert-audio-to-mp3.md) | POST | Creates an MP3 conversion job in Eranol. |
| [Convert Audio To WAV](actions/convert-audio-to-wav.md) | POST | Creates a WAV conversion job in Eranol. |
| [Convert Image To JPG](actions/convert-image-to-jpg.md) | POST | Creates a JPG conversion job in Eranol. |
| [Convert Image To WebP](actions/convert-image-to-webp.md) | POST | Creates a WebP conversion job in Eranol. |
| [Convert Video To MP4](actions/convert-video-to-mp4.md) | POST | Creates an MP4 conversion job in Eranol. |
| [Convert Video To WebM](actions/convert-video-to-webm.md) | POST | Creates a WebM conversion job in Eranol. |
| [Delete Job](actions/delete-job.md) | DELETE | Deletes an existing processing job from Eranol. |
| [Extract Audio From Video](actions/extract-audio-from-video.md) | POST | Creates an audio extraction job in Eranol. |
| [Get Job Status](actions/get-job-status.md) | GET | Retrieves the status of an Eranol job. |

### Media Job Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Result](actions/get-job-result.md) | GET | Retrieves the result of an Eranol job. |

