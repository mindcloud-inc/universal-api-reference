# Quiz Maker: Native API Reference

A consolidated summary of Quiz Maker's API configuration, with links to official documentation.

- **Official docs:** https://www.quiz-maker.com/Javascript-API
- **API base URL:** `https://www.quiz-maker.com/qapi`

## Authentication

### Public API Key

Use your Quiz Maker public API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.quiz-maker.com/Javascript-API)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

Response data is read from `list`.
