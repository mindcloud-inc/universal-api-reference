# Vocal Video: Native API Reference

A consolidated summary of Vocal Video's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://help.vocalvideo.com/article/23-using-the-subscription-api
- **API base URL:** `https://vocalvideo.com/api/v1`

## Authentication

### API Key

Use the Vocal Video workspace API key from Settings > API Key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.vocalvideo.com/article/23-using-the-subscription-api)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | `GET /account` | [docs](https://help.vocalvideo.com/article/23-using-the-subscription-api) |
| [List Replies](actions/list-replies.md) | `GET /replies` | [docs](https://help.vocalvideo.com/article/23-using-the-subscription-api) |
| [List Storyboards](actions/list-storyboards.md) | `GET /storyboards` | [docs](https://help.vocalvideo.com/article/23-using-the-subscription-api) |
| [Subscribe to Replies](actions/subscribe-to-replies.md) | `POST /replies/subscribe` | [docs](https://help.vocalvideo.com/article/23-using-the-subscription-api) |
| [Subscribe to Storyboards](actions/subscribe-to-storyboards.md) | `POST /storyboards/subscribe` | [docs](https://help.vocalvideo.com/article/23-using-the-subscription-api) |
| [Unsubscribe from Replies](actions/unsubscribe-from-replies.md) | `DELETE /replies/unsubscribe` | [docs](https://help.vocalvideo.com/article/23-using-the-subscription-api) |
| [Unsubscribe from Storyboards](actions/unsubscribe-from-storyboards.md) | `DELETE /storyboards/unsubscribe` | [docs](https://help.vocalvideo.com/article/23-using-the-subscription-api) |
