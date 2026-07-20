# Eranol: Native API Reference

A consolidated summary of Eranol's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://www.eranol.com/documentation
- **API base URL:** `https://eranol.com/api/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://www.eranol.com/documentation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Background Audio](actions/add-background-audio.md) | `POST /ffmpeg/video/add-bg-audio` | [docs](https://www.eranol.com/documentation) |
| [Add Intro](actions/add-intro.md) | `POST /ffmpeg/video/add-intro` | [docs](https://www.eranol.com/documentation) |
| [Add Outro](actions/add-outro.md) | `POST /ffmpeg/video/add-outro` | [docs](https://www.eranol.com/documentation) |
| [Convert Audio To MP3](actions/convert-audio-to-mp3.md) | `POST /ffmpeg/convert/audio/to/mp3` | [docs](https://www.eranol.com/documentation) |
| [Convert Audio To WAV](actions/convert-audio-to-wav.md) | `POST /ffmpeg/convert/audio/to/wav` | [docs](https://www.eranol.com/documentation) |
| [Convert Image To JPG](actions/convert-image-to-jpg.md) | `POST /ffmpeg/convert/image/to/jpg` | [docs](https://www.eranol.com/documentation) |
| [Convert Image To WebP](actions/convert-image-to-webp.md) | `POST /ffmpeg/convert/image/to/webp` | [docs](https://www.eranol.com/documentation) |
| [Convert Video To MP4](actions/convert-video-to-mp4.md) | `POST /ffmpeg/convert/video/to/mp4` | [docs](https://www.eranol.com/documentation) |
| [Convert Video To WebM](actions/convert-video-to-webm.md) | `POST /ffmpeg/convert/video/to/webm` | [docs](https://www.eranol.com/documentation) |
| [Delete Job](actions/delete-job.md) | `DELETE /ffmpeg/jobs/:job_id` | [docs](https://www.eranol.com/documentation) |
| [Extract Audio From Video](actions/extract-audio-from-video.md) | `POST /ffmpeg/video/extract/audio` | [docs](https://www.eranol.com/documentation) |
| [Get Job Result](actions/get-job-result.md) | `GET /ffmpeg/result/:job_id` | [docs](https://www.eranol.com/documentation) |
| [Get Job Status](actions/get-job-status.md) | `GET /ffmpeg/status/:job_id` | [docs](https://www.eranol.com/documentation) |
| [Verify API Key](actions/verify-api-key.md) | `GET /verify` | [docs](https://www.eranol.com/documentation) |
