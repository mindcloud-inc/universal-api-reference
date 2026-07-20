# Google PageSpeed Insights: Native API Reference

A consolidated summary of Google PageSpeed Insights's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://developers.google.com/speed/docs/insights/v5/get-started
- **API base URL:** `https://pagespeedonline.googleapis.com/pagespeedonline/v5`

## Authentication

### API Key

Use a Google Cloud API key enabled for the PageSpeed Insights API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.cloud.google.com/docs/authentication/api-keys?hl=en)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Analyze Page Speed](actions/analyze-page-speed.md) | `GET runPagespeed` | [docs](https://developers.google.com/speed/docs/insights/rest/v5/pagespeedapi/runpagespeed) |
