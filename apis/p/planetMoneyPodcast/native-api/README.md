# Planet Money Podcast: Native API Reference

A consolidated summary of Planet Money Podcast's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://www.npr.org/podcasts/510289/planet-money
- **API base URL:** `https://feeds.npr.org/510289`

## Authentication

### No Authentication

Public NPR RSS feed; no credentials required.

This API does not require request authentication.

[Official authentication documentation](https://www.npr.org/podcasts/510289/planet-money)

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get About Page](actions/get-about-page.md) | `GET https://www.npr.org/sections/money/2011/04/27/135599807/about-planet-money` | [docs](https://www.npr.org/sections/money/2011/04/27/135599807/about-planet-money) |
| [Get Episode Embed Player](actions/get-episode-embed-player.md) | `GET https://www.npr.org/player/embed/:storyId/:mediaId` | [docs](https://www.npr.org/player/embed/nx-s1-5751177/nx-s1-mx-5751177-1) |
| [Get Episode Transcript](actions/get-episode-transcript.md) | `GET https://www.npr.org/transcripts/:storyId` | [docs](https://www.npr.org/transcripts/nx-s1-5751177) |
| [Get Podcast Episode Page](actions/get-podcast-episode-page.md) | `GET https://www.npr.org/:year/:month/:day/:storyId/:slug` | [docs](https://www.npr.org/2026/03/20/nx-s1-5751177/book-deal-proposal-auction-publishing) |
| [Get Podcast Show Page](actions/get-podcast-show-page.md) | `GET https://www.npr.org/podcasts/510289/planet-money` | [docs](https://www.npr.org/podcasts/510289/planet-money) |
| [List Podcast Archive](actions/list-podcast-archive.md) | `GET https://www.npr.org/podcasts/510289/planet-money/partials` | [docs](https://www.npr.org/podcasts/510289/planet-money/partials?start=10) |
| [List Recent Episodes](actions/list-recent-episodes.md) | `GET /podcast.xml` | [docs](https://feeds.npr.org/510289/podcast.xml) |
