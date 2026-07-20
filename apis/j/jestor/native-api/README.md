# Jestor: Native API Reference

A consolidated summary of Jestor's API configuration, with links to official documentation.

- **Official docs:** https://docs.jestor.com/reference/getting-started-with-your-api
- **API base URL:** `https://3862da4ad0574f31be61ba0c914e4d29.api.jestor.com`

## Authentication

### API Key

Use a Jestor API token. MindCloud sends it using Jestor's documented bearer header format.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.jestor.com/reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.
