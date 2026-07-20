# Verbatik: Native API Reference

A consolidated summary of Verbatik's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://docs.verbatik.com/docs/api
- **API base URL:** `https://api.verbatik.com/api`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.verbatik.com/docs/api/authentication)

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Custom Voice Speech](actions/create-custom-voice-speech.md) | `POST /v1/voice-cloning` | [docs](https://docs.verbatik.com/docs/api/voice-cloning) |
| [Create Music](actions/create-music.md) | `POST /v1/text-to-music` | [docs](https://docs.verbatik.com/docs/api/text-to-music) |
| [Create Speech](actions/create-speech.md) | `POST /v1/tts` | [docs](https://docs.verbatik.com/docs/api/text-to-speech) |
| [Create Voice Clone](actions/create-voice-clone.md) | `POST /v1/voice-training` | [docs](https://docs.verbatik.com/docs/api/voice-cloning) |
| [Create Voice Design](actions/create-voice-design.md) | `POST /v1/voice-design` | [docs](https://docs.verbatik.com/docs/api/voice-design) |
| [List My Voices](actions/list-my-voices.md) | `GET /v1/my-voices` | [docs](https://docs.verbatik.com/docs/api/voice-cloning) |
| [List Voices](actions/list-voices.md) | `GET /v1/voices` | [docs](https://docs.verbatik.com/docs/api/voice-library) |
| [Upload Audio](actions/upload-audio.md) | `POST /audio-upload` | [docs](https://docs.verbatik.com/docs/api/voice-cloning) |
