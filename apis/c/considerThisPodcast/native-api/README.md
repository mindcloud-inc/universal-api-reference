# Consider This Podcast: Native API Reference

A consolidated summary of Consider This Podcast's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://www.npr.org/podcasts/510355/considerthis
- **API base URL:** `https://feeds.npr.org`

## Authentication

### No Authentication

Uses NPR's public podcast RSS feed. No credentials are required.

This API does not require request authentication.

[Official authentication documentation](https://feeds.npr.org/510355/podcast.xml)

## API conventions

Request bodies use XML.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/rss+xml, application/xml, text/xml` |
| `Content-Type` | `application/xml` |

Responses from this API use XML. Response data is read from `rss.channel.item`.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Episodes](actions/list-episodes.md) | `GET /510355/podcast.xml` | [docs](https://feeds.npr.org/510355/podcast.xml) |
