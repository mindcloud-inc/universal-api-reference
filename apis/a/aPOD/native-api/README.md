# APOD: Native API Reference

A consolidated summary of APOD's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://api.nasa.gov/#apod
- **API base URL:** `https://api.nasa.gov`

## Authentication

### NASA API Key

Use a NASA api.nasa.gov key in the `api_key` query parameter.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.nasa.gov/#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Astronomy Picture by Date](actions/get-astronomy-picture-by-date.md) | `GET /planetary/apod` | [docs](https://api.nasa.gov/#apod) |
| [Get Random Astronomy Pictures](actions/get-random-astronomy-pictures.md) | `GET /planetary/apod` | [docs](https://api.nasa.gov/#apod) |
| [Get Today's Astronomy Picture](actions/get-todays-astronomy-picture.md) | `GET /planetary/apod` | [docs](https://api.nasa.gov/#apod) |
| [List Astronomy Pictures by Date Range](actions/list-astronomy-pictures-by-date-range.md) | `GET /planetary/apod` | [docs](https://api.nasa.gov/#apod) |
