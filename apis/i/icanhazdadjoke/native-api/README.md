# icanhazdadjoke: Native API Reference

A consolidated summary of icanhazdadjoke's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://icanhazdadjoke.com/api
- **API base URL:** `https://icanhazdadjoke.com`

## Authentication

### No Authentication

No authentication is required for the icanhazdadjoke API.

This API does not require request authentication.

[Official authentication documentation](https://icanhazdadjoke.com/api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `User-Agent` | `MindCloud icanhazdadjoke App (https://mindcloud.co)` |

Responses from this API use JSON. The total page count is read from `total_pages`. The current page number is read from `current_page`.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–30). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Fetch Dad Joke](actions/fetch-dad-joke.md) | `GET /j/:jokeId` | [docs](https://icanhazdadjoke.com/api) |
| [Fetch Random Dad Joke](actions/fetch-random-dad-joke.md) | `GET /` | [docs](https://icanhazdadjoke.com/api) |
| [Fetch Random Slack Dad Joke](actions/fetch-random-slack-dad-joke.md) | `GET /slack` | [docs](https://icanhazdadjoke.com/api) |
| [Search Dad Jokes](actions/search-dad-jokes.md) | `GET /search` | [docs](https://icanhazdadjoke.com/api) |
