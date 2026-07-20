# AiVOOV: Native API Reference

A consolidated summary of AiVOOV's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/5434397/2sB2qXki3a
- **API base URL:** `https://aivoov.com/api/v8`

## Authentication

### API Key

Use your AiVOOV API key from Profile > API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://github.com/AiVOOV/aivoov-api)

## API conventions

Response data is read from `data`.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Audio](actions/create-audio.md) | `POST /create` | [docs](https://github.com/AiVOOV/aivoov-api#create-audio-with-multiple-voice-and-text-inputs) |
| [List Voices](actions/list-voices.md) | `GET /voices` | [docs](https://github.com/AiVOOV/aivoov-api#get-all-voice-ids) |
