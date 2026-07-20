# Bookoly: Native API Reference

A consolidated summary of Bookoly's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://bookoly.com/docs/api/v1
- **API base URL:** `https://bookoly.com/api/v1`

## Authentication

### API Key

Connect with a Bookoly API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://bookoly.com/docs/api/v1)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Audio To Video](actions/add-audio-to-video.md) | `POST /add-audio-to-video` | [docs](https://bookoly.com/docs/api/v1#/paths/~1add-audio-to-video/post) |
| [Add Audio With Subtitle To Video](actions/add-audio-with-subtitle-to-video.md) | `POST /add-audio-with-subtitle-to-video` | [docs](https://bookoly.com/docs/api/v1#/paths/~1add-audio-with-subtitle-to-video/post) |
| [Add Subtitle To Video](actions/add-subtitle-to-video.md) | `POST /add-subtitle-to-video` | [docs](https://bookoly.com/docs/api/v1#/paths/~1add-subtitle-to-video/post) |
| [Add Subtitle To Video From File](actions/add-subtitle-to-video-from-file.md) | `POST /add-subtitle-to-video-from-file` | [docs](https://bookoly.com/docs/api/v1#/paths/~1add-subtitle-to-video-from-file/post) |
| [Add Watermark To Video](actions/add-watermark-to-video.md) | `POST /add-watermark-to-video` | [docs](https://bookoly.com/docs/api/v1#/paths/~1add-watermark-to-video/post) |
| [Blur Video](actions/blur-video.md) | `POST /blur-a-video` | [docs](https://bookoly.com/docs/api/v1#/paths/~1blur-a-video/post) |
| [Clip Video](actions/clip-video.md) | `POST /clip-a-video` | [docs](https://bookoly.com/docs/api/v1#/paths/~1clip-a-video/post) |
| [Combine Sounds](actions/combine-sounds.md) | `POST /combine-sounds` | [docs](https://bookoly.com/docs/api/v1#/paths/~1combine-sounds/post) |
| [Create Speech Dialogue](actions/create-speech-dialogue.md) | `POST /create-speech-dialogue` | [docs](https://bookoly.com/docs/api/v1#/paths/~1create-speech-dialogue/post) |
| [Create Speech Synthesis](actions/create-speech-synthesis.md) | `POST /text-to-speech` | [docs](https://bookoly.com/docs/api/v1#/paths/~1text-to-speech/post) |
| [Create Transcript](actions/create-transcript.md) | `POST /create-transcript` | [docs](https://bookoly.com/docs/api/v1#/paths/~1create-transcript/post) |
| [Create Video](actions/create-video.md) | `POST https://bookoly.com/api/v2/generate-a-video` | [docs](https://bookoly.com/docs/api/v2#/paths/~1generate-a-video/post) |
| [Create Video From Images/Videos](actions/create-video-from-images-videos.md) | `POST /assets-to-video` | [docs](https://bookoly.com/docs/api/v1#/paths/~1assets-to-video/post) |
| [Crop Video](actions/crop-video.md) | `POST /crop-a-video` | [docs](https://bookoly.com/docs/api/v1#/paths/~1crop-a-video/post) |
| [Extract Audio From Video](actions/extract-audio-from-video.md) | `POST /extract-audio-from-video` | [docs](https://bookoly.com/docs/api/v1#/paths/~1extract-audio-from-video/post) |
| [Frame Video](actions/frame-video.md) | `POST /frame-a-video` | [docs](https://bookoly.com/docs/api/v1#/paths/~1frame-a-video/post) |
| [Generate Subtitle File](actions/generate-subtitle-file.md) | `POST /generate-subtitle-file` | [docs](https://bookoly.com/docs/api/v1#/paths/~1generate-subtitle-file/post) |
| [Get Sound](actions/get-sound.md) | `GET /sounds/{sound}` | [docs](https://bookoly.com/docs/api/v1#/paths/~1sounds~1{sound}/get) |
| [Get Speech](actions/get-speech.md) | `GET /speeches/{speech}` | [docs](https://bookoly.com/docs/api/v1#/paths/~1speeches~1{speech}/get) |
| [Get Speech Dialogue](actions/get-speech-dialogue.md) | `GET /speechDialogues/{speechDialogue}` | [docs](https://bookoly.com/docs/api/v1#/paths/~1speechDialogues~1{speechDialogue}/get) |
| [Get Subtitle File](actions/get-subtitle-file.md) | `GET /subtitleFiles/{subtitleFile}` | [docs](https://bookoly.com/docs/api/v1#/paths/~1subtitleFiles~1{subtitleFile}/get) |
| [Get Transcript](actions/get-transcript.md) | `GET /transcripts/{transcript}` | [docs](https://bookoly.com/docs/api/v1#/paths/~1transcripts~1{transcript}/get) |
| [Get User](actions/get-user.md) | `GET /users/{user}` | [docs](https://bookoly.com/docs/api/v1#/paths/~1users~1{user}/get) |
| [Get Video](actions/get-video.md) | `GET /videos/{video}` | [docs](https://bookoly.com/docs/api/v1#/paths/~1videos~1{video}/get) |
| [Mute Video](actions/mute-video.md) | `POST /mute-a-video` | [docs](https://bookoly.com/docs/api/v1#/paths/~1mute-a-video/post) |
| [Overlay Videos](actions/overlay-videos.md) | `POST /overlay-videos` | [docs](https://bookoly.com/docs/api/v1#/paths/~1overlay-videos/post) |
| [Rotate Video](actions/rotate-video.md) | `POST /rotate-a-video` | [docs](https://bookoly.com/docs/api/v1#/paths/~1rotate-a-video/post) |
| [Scale Video](actions/scale-video.md) | `POST /scale-a-video` | [docs](https://bookoly.com/docs/api/v1#/paths/~1scale-a-video/post) |
| [Split Video Into Scenes](actions/split-video-into-scenes.md) | `POST /split-video-into-scenes` | [docs](https://bookoly.com/docs/api/v1#/paths/~1split-video-into-scenes/post) |
| [Stack Videos](actions/stack-videos.md) | `POST /stack-videos` | [docs](https://bookoly.com/docs/api/v1#/paths/~1stack-videos/post) |
| [Validate API Token](actions/validate-api-token.md) | `POST /auth-check` | [docs](https://bookoly.com/docs/api/v1) |
