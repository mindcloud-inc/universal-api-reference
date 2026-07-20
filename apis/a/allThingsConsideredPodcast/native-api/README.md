# All Things Considered Podcast: Native API Reference

A consolidated summary of All Things Considered Podcast's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://www.npr.org/programs/all-things-considered/archive
- **REST API base URL:** `https://www.npr.org`
- **REST API base URL:** `https://feeds.npr.org`

## Authentication

### No authentication

Public NPR archive RSS feed and linked story pages do not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://www.npr.org/programs/all-things-considered/archive)

## API conventions

### REST API

Responses from this API use XML.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Embedded Player Metadata](actions/get-embedded-player-metadata.md) | `GET /player/embed/:storyId/:mediaId` | [docs](https://www.npr.org/player/embed/nx-s1-5803566/nx-s1-9750301) |
| [Get Feed Metadata](actions/get-feed-metadata.md) | `GET https://feeds.npr.org/2/rss.xml` | [docs](https://feeds.npr.org/2/rss.xml) |
| [Get Story Audio Metadata](actions/get-story-audio-metadata.md) | `GET /:year/:month/:day/:storyId/:slug` | [docs](https://www.npr.org/2026/04/29/nx-s1-5803566/musk-continued-his-testimony-from-yesterday-in-lawsuit-against-openai) |
| [Get Story Details](actions/get-story-details.md) | `GET /:year/:month/:day/:storyId/:slug` | [docs](https://www.npr.org/2026/04/29/nx-s1-5803566/musk-continued-his-testimony-from-yesterday-in-lawsuit-against-openai) |
| [Get Story Transcript](actions/get-story-transcript.md) | `GET /transcripts/:storyId` | [docs](https://www.npr.org/transcripts/nx-s1-5803566) |
| [List Archive Shows](actions/list-archive-shows.md) | `GET /programs/all-things-considered/archive` | [docs](https://www.npr.org/programs/all-things-considered/archive) |
| [List Archive Shows By Date](actions/list-archive-shows-by-date.md) | `GET /programs/all-things-considered/archive` | [docs](https://www.npr.org/programs/all-things-considered/archive) |
| [List Stories](actions/list-stories.md) | `GET https://feeds.npr.org/2/rss.xml` | [docs](https://feeds.npr.org/2/rss.xml) |
