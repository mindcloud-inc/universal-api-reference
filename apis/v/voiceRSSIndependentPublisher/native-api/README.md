# VoiceRSS (Independent Publisher): Native API Reference

A consolidated summary of VoiceRSS (Independent Publisher)'s API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://www.voicerss.org/api/
- **API base URL:** `https://api.voicerss.org`

## Authentication

### API Key

Authenticate requests with a VoiceRSS API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.voicerss.org/api/)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use plain text.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Convert Text to Speech](actions/convert-text-to-speech.md) | `GET /` | [docs](https://www.voicerss.org/api/) |
