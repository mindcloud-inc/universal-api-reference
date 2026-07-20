# Humor API: Native API Reference

A consolidated summary of Humor API's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://humorapi.com/docs/
- **OpenAPI specification:** https://raw.githubusercontent.com/ddsky/humor-api-clients/refs/heads/main/humorapi-openapi-3.json
- **API base URL:** `https://api.humorapi.com`

## Authentication

### API Key

Use your Humor API key from https://humorapi.com/. Requests are authenticated with the api-key query parameter.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://humorapi.com/docs)

## API conventions

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `api-key` | query | `string` | no | Injected from your connected API key credential. |

## Pagination

Use `number` in the query string to set the page size (default 10; accepted range 0–10). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Analyze Joke](actions/analyze-joke.md) | `POST /jokes/analyze` | [docs](https://humorapi.com/docs/#Analyze-Joke) |
| [Create Joke](actions/create-joke.md) | `GET /jokes/create` | [docs](https://humorapi.com/docs/#Create-Joke) |
| [Downvote Joke](actions/downvote-joke.md) | `POST /jokes/:id/downvote` | [docs](https://humorapi.com/docs/#Downvote-Joke) |
| [Downvote Meme](actions/downvote-meme.md) | `POST /memes/{id}/downvote` | [docs](https://humorapi.com/docs/#Downvote-Meme) |
| [Generate Nonsense Word](actions/generate-nonsense-word.md) | `GET /words/nonsense/random` | [docs](https://humorapi.com/docs/#Generate-Nonsense-Word) |
| [Get Random Joke](actions/get-random-joke.md) | `GET /jokes/random` | [docs](https://humorapi.com/docs/#Random-Joke) |
| [Get Random Meme](actions/get-random-meme.md) | `GET /memes/random` | [docs](https://humorapi.com/docs/#Random-Meme) |
| [Insult](actions/insult.md) | `GET /insult` | [docs](https://humorapi.com/docs/#Insult) |
| [Praise](actions/praise.md) | `GET /praise` | [docs](https://humorapi.com/docs/#Praise) |
| [Rate Word](actions/rate-word.md) | `GET /words/rate` | [docs](https://humorapi.com/docs/#Rate-Word) |
| [Search Gifs](actions/search-gifs.md) | `GET /gif/search` | [docs](https://humorapi.com/docs/#Search-Gifs) |
| [Search Jokes](actions/search-jokes.md) | `GET /jokes/search` | [docs](https://humorapi.com/docs/#Search-Jokes) |
| [Search Memes](actions/search-memes.md) | `GET /memes/search` | [docs](https://humorapi.com/docs/#Search-Memes) |
| [Submit Joke](actions/submit-joke.md) | `POST /jokes` | [docs](https://humorapi.com/docs/#Submit-Joke) |
| [Upvote Joke](actions/upvote-joke.md) | `POST /jokes/:id/upvote` | [docs](https://humorapi.com/docs/#Upvote-Joke) |
| [Upvote Meme](actions/upvote-meme.md) | `POST /memes/:id/upvote` | [docs](https://humorapi.com/docs/#Upvote-Meme) |
