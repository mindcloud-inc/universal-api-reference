# MyOwnConference: Native API Reference

A consolidated summary of MyOwnConference's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://support.myownconference.com/en/article/myownconference-public-api-o6or9a/
- **API base URL:** `https://api.mywebinar.com`

## Authentication

### API key

Use the API key from the MyOwnConference Profile page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.myownconference.com/en/article/myownconference-public-api-o6or9a/)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

Response data is read from `response`.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get profile](actions/get-profile.md) | `POST /` | [docs](https://support.myownconference.com/en/article/myownconference-public-api-o6or9a/) |
| [List webinars](actions/list-webinars.md) | `POST /` | [docs](https://support.myownconference.com/en/article/myownconference-public-api-o6or9a/) |
