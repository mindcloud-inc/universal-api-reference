# Creator Science Podcast: Native API Reference

A consolidated summary of Creator Science Podcast's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://podcast.creatorscience.com
- **API base URL:** `https://feeds.megaphone.fm`

## Authentication

### No Authentication

Public RSS feed access over HTTPS GET; no credentials are required.

This API does not require request authentication.

[Official authentication documentation](https://feeds.megaphone.fm/TPG4024225475)

## API conventions

Request bodies use XML.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/rss+xml, application/xml` |
| `Content-Type` | `application/xml` |

Responses from this API use XML. Response data is read from `rss.channel.item`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Podcast Episodes](actions/list-podcast-episodes.md) | `GET /TPG4024225475` | [docs](https://feeds.megaphone.fm/TPG4024225475) |
