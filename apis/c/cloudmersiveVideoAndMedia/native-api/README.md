# Cloudmersive Video and Media: Native API Reference

A consolidated summary of Cloudmersive Video and Media's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://api.cloudmersive.com/docs/video.asp
- **OpenAPI specification:** https://api.cloudmersive.com/video/docs/v1/swagger
- **API base URL:** `https://api.cloudmersive.com`

## Authentication

### API Key

Cloudmersive API key authentication using the Apikey request header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Apikey: <apiKey>
```

[Official authentication documentation](https://api.cloudmersive.com/docs/video.asp#Authentication)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Convert Audio to MP3](actions/convert-audio-to-mp3.md) | `POST /video/convert/to/mp3` | [docs](https://api.cloudmersive.com/docs/video.asp#operation--video-convert-to-mp3-post) |
| [Get Media Information](actions/get-media-information.md) | `POST /video/convert/get-info` | [docs](https://api.cloudmersive.com/docs/video.asp#operation--video-convert-get-info-post) |
