# NASA APOD: Native API Reference

A consolidated summary of NASA APOD's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://api.nasa.gov/
- **API base URL:** `https://api.nasa.gov`

## Authentication

### NASA API Key

NASA API key used as the shared api_key query parameter.

### Credentials

- **NASA API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.nasa.gov/assets/html/authentication.html)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 250 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get APOD Date Range](actions/get-apod-date-range.md) | `GET /planetary/apod` | [docs](https://api.nasa.gov/) |
| [Get Astronomy Picture of the Day](actions/get-astronomy-picture-of-the-day.md) | `GET /planetary/apod` | [docs](https://api.nasa.gov/) |
| [Get Random APODs](actions/get-random-apods.md) | `GET /planetary/apod` | [docs](https://api.nasa.gov/) |
