# Fresh Air Podcast: Native API Reference

A consolidated summary of Fresh Air Podcast's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://www.npr.org/podcasts/381444908/fresh-air
- **API base URL:** `https://feeds.npr.org`

## Authentication

### No Authentication

This app reads NPR's public Fresh Air RSS feed and does not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://www.npr.org/podcasts/381444908/fresh-air)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/rss+xml, application/xml, text/xml;q=0.9, application/atom+xml;q=0.8, */*;q=0.1` |

Responses from this API use XML. Response data is read from `rss.channel.item`.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Episodes](actions/list-episodes.md) | `GET /381444908/podcast.xml` | [docs](https://www.npr.org/podcasts/381444908/fresh-air) |
