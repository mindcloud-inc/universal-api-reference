# WhatIsMyBrowser: Native API Reference

A consolidated summary of WhatIsMyBrowser's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://developers.whatismybrowser.com/api/docs/v3/integration-guide/
- **API base URL:** `https://api.whatismybrowser.com/api/v3`

## Authentication

### API Key

Authenticate by sending the account API key in the X-API-KEY HTTP header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://developers.whatismybrowser.com/api/docs/v3/integration-guide/common-elements/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Detect Headers](actions/detect-headers.md) | `POST /detect` | [docs](https://developers.whatismybrowser.com/api/docs/v3/integration-guide/detect/requests/) |
| [Get Version Numbers](actions/get-version-numbers.md) | `GET /version_numbers` | [docs](https://developers.whatismybrowser.com/api/docs/v3/integration-guide/version-numbers/requests/) |
