# Quanta Science Podcast: Native API Reference

A consolidated summary of Quanta Science Podcast's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://www.quantamagazine.org/tag/quanta-podcast/
- **API base URL:** `https://quantapodcast.quantamagazine.org`

## Authentication

### No Authentication

No credentials are required to read the public Quanta podcast RSS feed.

This API does not require request authentication.

[Official authentication documentation](https://www.quantamagazine.org/tag/quanta-podcast/)

## API conventions

Responses from this API use XML. Response data is read from `rss.channel.item`.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Podcast Episodes](actions/list-podcast-episodes.md) | `GET /` | [docs](https://www.quantamagazine.org/tag/quanta-podcast/) |
