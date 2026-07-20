# Darknet Diaries Podcast: Native API Reference

A consolidated summary of Darknet Diaries Podcast's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://darknetdiaries.com
- **API base URL:** `https://podcast.darknetdiaries.com`

## Authentication

### Public RSS Feed

Access the Darknet Diaries podcast through its public RSS feed.

This API does not require request authentication.

[Official authentication documentation](https://darknetdiaries.com)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/rss+xml` |
| `Content-Type` | `application/rss+xml` |

Responses from this API use XML. Response data is read from `rss.channel`.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Episode By GUID](actions/get-episode-by-guid.md) | `GET /` | [docs](https://podcast.darknetdiaries.com) |
| [Get Episode By Number](actions/get-episode-by-number.md) | `GET /` | [docs](https://podcast.darknetdiaries.com) |
| [Get Latest Episode](actions/get-latest-episode.md) | `GET /` | [docs](https://podcast.darknetdiaries.com) |
| [Get Podcast Artwork](actions/get-podcast-artwork.md) | `GET /` | [docs](https://podcast.darknetdiaries.com) |
| [Get Podcast Feed Information](actions/get-podcast-feed-information.md) | `GET /` | [docs](https://podcast.darknetdiaries.com) |
| [Get Podcast Metadata](actions/get-podcast-metadata.md) | `GET /` | [docs](https://podcast.darknetdiaries.com) |
| [List Clean Episodes](actions/list-clean-episodes.md) | `GET /` | [docs](https://podcast.darknetdiaries.com) |
| [List Episode Artwork](actions/list-episode-artwork.md) | `GET /` | [docs](https://podcast.darknetdiaries.com) |
| [List Episode Audio Assets](actions/list-episode-audio-assets.md) | `GET /` | [docs](https://podcast.darknetdiaries.com) |
| [List Episode Transcripts](actions/list-episode-transcripts.md) | `GET /` | [docs](https://podcast.darknetdiaries.com) |
| [List Episodes](actions/list-episodes.md) | `GET /` | [docs](https://podcast.darknetdiaries.com) |
| [List Episodes By Date Range](actions/list-episodes-by-date-range.md) | `GET /` | [docs](https://podcast.darknetdiaries.com) |
| [List Episodes Published After](actions/list-episodes-published-after.md) | `GET /` | [docs](https://podcast.darknetdiaries.com) |
| [List Episodes Published Before](actions/list-episodes-published-before.md) | `GET /` | [docs](https://podcast.darknetdiaries.com) |
| [List Episodes With Transcripts](actions/list-episodes-with-transcripts.md) | `GET /` | [docs](https://podcast.darknetdiaries.com) |
| [List Episodes Without Transcripts](actions/list-episodes-without-transcripts.md) | `GET /` | [docs](https://podcast.darknetdiaries.com) |
| [List Explicit Episodes](actions/list-explicit-episodes.md) | `GET /` | [docs](https://podcast.darknetdiaries.com) |
| [List Recent Episodes](actions/list-recent-episodes.md) | `GET /` | [docs](https://podcast.darknetdiaries.com) |
| [Search Episodes By Summary](actions/search-episodes-by-summary.md) | `GET /` | [docs](https://podcast.darknetdiaries.com) |
| [Search Episodes By Title](actions/search-episodes-by-title.md) | `GET /` | [docs](https://podcast.darknetdiaries.com) |
