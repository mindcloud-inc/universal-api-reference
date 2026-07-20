# PushCallMe: Native API Reference

A consolidated summary of PushCallMe's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://pushcall.me/docs/phone-call-via-http-api
- **API base URL:** `https://pushcall.me`

## Authentication

### API Key

Authenticate PushCall requests with your PushCall API key sent as the api_key query parameter.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://pushcall.me/docs/phone-call-via-http-api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Call Status](actions/get-call-status.md) | `GET /api/calls/:requestId` | [docs](https://pushcall.me/docs/phone-call-via-http-api) |
| [Make Phone Call](actions/make-phone-call.md) | `GET /api/call` | [docs](https://pushcall.me/docs/phone-call-via-http-api) |
