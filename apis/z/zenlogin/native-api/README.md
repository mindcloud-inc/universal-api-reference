# Zenlogin: Native API Reference

A consolidated summary of Zenlogin's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://zenlogin.co/docs
- **API base URL:** `https://api.zenlogin.co/v1`

## Authentication

### API Key

Authenticate Zenlogin API requests with the account secret key in the `X_API_SECRET_KEY` request header.

### Credentials

- **API Key:** `apiKey` · required
- **Application Key:** `applicationKey` · required · Zenlogin application key from the API endpoint path, between /applications/ and /logins/checks.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://zenlogin.co/docs)

## API conventions

Response data is read from `data`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Login Check](actions/create-login-check.md) | `POST /applications/[:application_key]/logins/checks` | [docs](https://zenlogin.co/docs) |
