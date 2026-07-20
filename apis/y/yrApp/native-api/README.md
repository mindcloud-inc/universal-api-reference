# Yr app: Native API Reference

A consolidated summary of Yr app's API configuration, with links to official documentation.

- **Official docs:** https://api.met.no/weatherapi/documentation
- **API base URL:** `https://api.met.no/weatherapi`

## Authentication

### No Authentication

The public MET Weather API endpoints used by Yr do not require stored credentials; requests must include an identifying User-Agent header.

This API does not require request authentication.

[Official authentication documentation](https://api.met.no/weatherapi/documentation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |
| `User-Agent` | `MindCloud Yr app/1.0 (apps@mindcloud.co)` |

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.
