# Humantic AI: Native API Reference

A consolidated summary of Humantic AI's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://api.humantic.ai/
- **API base URL:** `https://api.humantic.ai/v1`

## Authentication

### API Key

Humantic AI API key authentication. The provider expects the key as the shared `apikey` query parameter on API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.humantic.ai/)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Document Analysis](actions/create-document-analysis.md) | `POST /user-profile/create` | [docs](https://api.humantic.ai/) |
| [Create Profile Analysis](actions/create-profile-analysis.md) | `GET /user-profile/create` | [docs](https://api.humantic.ai/) |
| [Create Text Analysis](actions/create-text-analysis.md) | `POST /user-profile/create` | [docs](https://api.humantic.ai/) |
| [Fetch Analysis](actions/fetch-analysis.md) | `GET /user-profile/` | [docs](https://api.humantic.ai/) |
| [Update Analysis With Text](actions/update-analysis-with-text.md) | `POST /user-profile/create` | [docs](https://api.humantic.ai/) |
