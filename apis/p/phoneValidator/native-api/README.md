# Phone Validator: Native API Reference

A consolidated summary of Phone Validator's API configuration, with links to official documentation.

- **Official docs:** https://www.phonevalidator.com/ApiDoc/V3/
- **API base URL:** `https://api.phonevalidator.com`

## Authentication

### API Key

Authenticate requests with the Phone Validator API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.phonevalidator.com/ApiDoc/V3/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.
