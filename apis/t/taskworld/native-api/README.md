# Taskworld: Native API Reference

A consolidated summary of Taskworld's API configuration, with links to official documentation.

- **Official docs:** https://api-docs.taskworld.com/
- **API base URL:** `https://us.taskworld.com/api/public/v1`

## Authentication

### Taskworld Access Token

Authenticate Taskworld API requests with an access token returned by /v1/auth.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api-docs.taskworld.com/)

### Taskworld Body Access Token

Authenticate Taskworld API requests using access_token in request body.

### Credentials

- **Access Token:** `accessToken` · required · Taskworld access token from /v1/auth response.

[Official authentication documentation](https://api-docs.taskworld.com/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the request body to set the page size (default 25).
