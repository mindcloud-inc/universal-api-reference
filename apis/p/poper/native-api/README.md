# Poper: Native API Reference

A consolidated summary of Poper's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://support.poper.ai/en/collections/10876722-api
- **API base URL:** `https://api.poper.ai/general/v1`

## Authentication

### API Key

Connect Poper with an API key created in Settings -> API Keys.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.poper.ai/en/articles/10095373-setting-up-and-authenticating-your-api-key)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Popup Responses](actions/list-popup-responses.md) | `POST /popup/responses` | [docs](https://support.poper.ai/en/articles/10095372-view-popup-responses) |
| [List Popups](actions/list-popups.md) | `POST /popup/list` | [docs](https://support.poper.ai/en/articles/10095374-list-all-popups) |
| [Verify API Key](actions/verify-api-key.md) | `POST /ping` | [docs](https://support.poper.ai/en/articles/10095373-setting-up-and-authenticating-your-api-key) |
