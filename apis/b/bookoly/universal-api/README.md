# <img src="https://images.mindcloud.co/apps/icons/bookoly_1776105324870.png" alt="Bookoly logo" width="28" height="28"> Bookoly: Universal API

Create videos, subtitles, speech, and transcripts with Bookoly

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bookoly/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bookoly.com
- **Vendor API docs:** https://bookoly.com/docs/api/v1

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate API Token](actions/validate-api-token.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookoly/latest/actions/validate-api-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Api Token

| Action | Method | Description |
| --- | --- | --- |
| [Validate API Token](actions/validate-api-token.md) | GET | Validates the current Bookoly API token. |

### Sound

| Action | Method | Description |
| --- | --- | --- |
| [Combine Sounds](actions/combine-sounds.md) | POST | Combines multiple sounds into one in Bookoly. |
| [Get Sound](actions/get-sound.md) | GET | Retrieves a specific sound from Bookoly. |

### Speech

| Action | Method | Description |
| --- | --- | --- |
| [Create Speech Synthesis](actions/create-speech-synthesis.md) | POST | Creates speech synthesis from text in Bookoly. |
| [Get Speech](actions/get-speech.md) | GET | Retrieves a specific speech from Bookoly. |

### Speech Dialogue

| Action | Method | Description |
| --- | --- | --- |
| [Create Speech Dialogue](actions/create-speech-dialogue.md) | POST | Creates a speech dialogue in Bookoly. |
| [Get Speech Dialogue](actions/get-speech-dialogue.md) | GET | Retrieves a specific speech dialogue from Bookoly. |

### Subtitle File

| Action | Method | Description |
| --- | --- | --- |
| [Generate Subtitle File](actions/generate-subtitle-file.md) | POST | Creates a subtitle file in Bookoly. |
| [Get Subtitle File](actions/get-subtitle-file.md) | GET | Retrieves a specific subtitle file from Bookoly. |

### Transcript

| Action | Method | Description |
| --- | --- | --- |
| [Create Transcript](actions/create-transcript.md) | POST | Creates a transcript from audio or video in Bookoly. |
| [Get Transcript](actions/get-transcript.md) | GET | Retrieves a specific transcript from Bookoly. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a specific user from Bookoly. |

### Video

| Action | Method | Description |
| --- | --- | --- |
| [Add Audio To Video](actions/add-audio-to-video.md) | POST | Adds audio to a video in Bookoly. |
| [Add Audio With Subtitle To Video](actions/add-audio-with-subtitle-to-video.md) | POST | Adds audio with subtitles to a video in Bookoly. |
| [Add Subtitle To Video](actions/add-subtitle-to-video.md) | POST | Adds subtitles to a video in Bookoly. |
| [Add Subtitle To Video From File](actions/add-subtitle-to-video-from-file.md) | POST | Adds subtitles from a file to a video in Bookoly. |
| [Add Watermark To Video](actions/add-watermark-to-video.md) | POST | Adds a watermark to a video in Bookoly. |
| [Blur Video](actions/blur-video.md) | POST | Blurs a selected area of a video in Bookoly. |
| [Clip Video](actions/clip-video.md) | POST | Clips a video to a selected segment in Bookoly. |
| [Create Video](actions/create-video.md) | POST | Creates a new video in Bookoly. |
| [Create Video From Images/Videos](actions/create-video-from-images-videos.md) | POST | Creates a video from images or videos in Bookoly. |
| [Crop Video](actions/crop-video.md) | POST | Crops a video to a selected area in Bookoly. |
| [Extract Audio From Video](actions/extract-audio-from-video.md) | POST | Extracts audio from a video in Bookoly. |
| [Frame Video](actions/frame-video.md) | POST | Creates a video frame image in Bookoly. |
| [Get Video](actions/get-video.md) | GET | Retrieves a specific video from Bookoly. |
| [Mute Video](actions/mute-video.md) | POST | Removes audio from a video in Bookoly. |
| [Overlay Videos](actions/overlay-videos.md) | POST | Creates an overlay video in Bookoly. |
| [Rotate Video](actions/rotate-video.md) | POST | Rotates a video by fixed degrees in Bookoly. |
| [Scale Video](actions/scale-video.md) | POST | Scales a video to new dimensions in Bookoly. |
| [Split Video Into Scenes](actions/split-video-into-scenes.md) | POST | Splits a video into scenes in Bookoly. |
| [Stack Videos](actions/stack-videos.md) | POST | Creates a stacked video in Bookoly. |

