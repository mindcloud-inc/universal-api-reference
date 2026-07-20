# TrueReview: Native API Reference

A consolidated summary of TrueReview's API configuration, with links to official documentation.

- **Official docs:** https://truereview.help/en/articles/9001450-truereview-api
- **API base URL:** `https://app.truereview.co/api/v1`

## Authentication

### API Key

Authenticate with your TrueReview account access token and target Location SID.

### Credentials

- **API Key:** `apiKey` · required
- **Location SID:** `locationSid` · required · The TrueReview Location SID for the business/location this connection should use.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://intercom.help/truereview/en/articles/9001450-truereview-api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.
