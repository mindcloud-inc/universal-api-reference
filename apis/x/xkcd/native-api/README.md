# Xkcd: Native API Reference

A consolidated summary of Xkcd's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://xkcd.com/json.html
- **API base URL:** `https://xkcd.com`

## Authentication

### No authentication

The official xkcd JSON interface is public and does not require authentication.

This API does not require request authentication.

[Official authentication documentation](https://xkcd.com/json.html)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Atom Feed](actions/get-atom-feed.md) | `GET /atom.xml` | [docs](https://xkcd.com/) |
| [Get Comic](actions/get-comic.md) | `GET /:comicNumber/info.0.json` | [docs](https://xkcd.com/json.html) |
| [Get Latest Comic](actions/get-latest-comic.md) | `GET /info.0.json` | [docs](https://xkcd.com/json.html) |
| [Get RSS Feed](actions/get-rss-feed.md) | `GET /rss.xml` | [docs](https://xkcd.com/) |
