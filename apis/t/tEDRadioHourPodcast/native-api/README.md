# TED Radio Hour Podcast: Native API Reference

A consolidated summary of TED Radio Hour Podcast's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://www.npr.org/podcasts/510298/ted-radio-hour
- **API base URL:** `https://feeds.npr.org`

## Authentication

### Public RSS Feed

No credentials required for the official NPR TED Radio Hour RSS feed.

This API does not require request authentication.

[Official authentication documentation](https://www.npr.org/podcasts/510298/ted-radio-hour)

## API conventions

Responses from this API use XML. Response data is read from `rss.channel.item`.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Episodes](actions/list-episodes.md) | `GET /510298/podcast.xml` | [docs](https://feeds.npr.org/510298/podcast.xml) |
