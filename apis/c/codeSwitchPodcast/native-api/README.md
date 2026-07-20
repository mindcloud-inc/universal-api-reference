# Code Switch Podcast: Native API Reference

A consolidated summary of Code Switch Podcast's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://www.npr.org/podcasts/510312/codeswitch
- **API base URL:** `https://feeds.npr.org`

## Authentication

### No Authentication

Public RSS feed; no authentication required.

This API does not require request authentication.

[Official authentication documentation](https://www.npr.org/podcasts/510312/codeswitch)

## API conventions

Responses from this API use XML. Response data is read from `rss.channel.item`.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Podcast Feed](actions/get-podcast-feed.md) | `GET /510312/podcast.xml` | [docs](https://www.npr.org/podcasts/510312/codeswitch) |
