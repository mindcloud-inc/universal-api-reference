# Meme API: Native API Reference

A consolidated summary of Meme API's API configuration and 4 documented operations.

- **API base URL:** `https://meme-api.com`

## Authentication

### No Authentication

This API does not require request authentication.

[Official authentication documentation](https://github.com/D3vd/Meme_Api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Fetch Memes From Subreddit](actions/fetch-memes-from-subreddit.md) | `GET /gimme/:subreddit/:count` | [docs](https://github.com/D3vd/Meme_Api) |
| [Fetch Random Meme](actions/fetch-random-meme.md) | `GET /gimme` | [docs](https://github.com/D3vd/Meme_Api) |
| [Fetch Random Meme From Subreddit](actions/fetch-random-meme-from-subreddit.md) | `GET /gimme/:subreddit` | [docs](https://github.com/D3vd/Meme_Api) |
| [Fetch Random Memes](actions/fetch-random-memes.md) | `GET /gimme/:count` | [docs](https://github.com/D3vd/Meme_Api) |
