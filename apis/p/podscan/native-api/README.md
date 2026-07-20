# Podscan: Native API Reference

A consolidated summary of Podscan's API configuration and 48 documented operations, with links to official documentation.

- **Official docs:** https://podscan.fm/docs/api
- **API base URL:** `https://podscan.fm/api/v1`

## Authentication

### API Key

Authenticate Podscan requests with a bearer API key from the Podscan dashboard.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://podscan.fm/docs/api)

## Pagination

Use `per_page` in the query string to set the page size (default 25; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (48 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Discover Similar Podcasts](actions/discover-similar-podcasts.md) | `GET /podcasts/{podcast}/discover` | [docs](https://podscan.fm/docs/api) |
| [Get Entity](actions/get-entity.md) | `GET /entities/{entityId}` | [docs](https://podscan.fm/docs/api) |
| [Get Episode](actions/get-episode.md) | `GET /episodes/{episode}` | [docs](https://podscan.fm/docs/api) |
| [Get Episode Brand Safety](actions/get-episode-brand-safety.md) | `GET /episodes/{episode}/brand-safety` | [docs](https://podscan.fm/docs/api) |
| [Get Episode Demographics](actions/get-episode-demographics.md) | `GET /episodes/{episode}/demographics` | [docs](https://podscan.fm/docs/api) |
| [Get Episode Engagement](actions/get-episode-engagement.md) | `GET /episodes/{episode}/engagement` | [docs](https://podscan.fm/docs/api) |
| [Get IAB Category](actions/get-iab-category.md) | `GET /iab-categories/{id}` | [docs](https://podscan.fm/docs/api) |
| [Get Latest Podcast Episode](actions/get-latest-podcast-episode.md) | `GET /podcasts/{podcast}/latest/episode` | [docs](https://podscan.fm/docs/api) |
| [Get Latest Podcast Guest](actions/get-latest-podcast-guest.md) | `GET /podcasts/{podcast}/latest/guest` | [docs](https://podscan.fm/docs/api) |
| [Get Latest Podcast Sponsor](actions/get-latest-podcast-sponsor.md) | `GET /podcasts/{podcast}/latest/sponsor` | [docs](https://podscan.fm/docs/api) |
| [Get Podcast](actions/get-podcast.md) | `GET /podcasts/{podcast}` | [docs](https://podscan.fm/docs/api) |
| [Get Podcast Analysis](actions/get-podcast-analysis.md) | `GET /podcasts/{podcast}/analysis` | [docs](https://podscan.fm/docs/api) |
| [Get Podcast Brand Safety](actions/get-podcast-brand-safety.md) | `GET /podcasts/{podcast}/brand-safety` | [docs](https://podscan.fm/docs/api) |
| [Get Podcast Chart History](actions/get-podcast-chart-history.md) | `GET /podcasts/{podcast}/chart-history` | [docs](https://podscan.fm/docs/api) |
| [Get Podcast Demographics](actions/get-podcast-demographics.md) | `GET /podcasts/{podcast}/demographics` | [docs](https://podscan.fm/docs/api) |
| [Get Publisher](actions/get-publisher.md) | `GET /publishers/{publisherId}` | [docs](https://podscan.fm/docs/api) |
| [Get Sponsor](actions/get-sponsor.md) | `GET /sponsors/{sponsor}` | [docs](https://podscan.fm/docs/api) |
| [Get Sponsor Trend](actions/get-sponsor-trend.md) | `GET /sponsors/{sponsor}/trend` | [docs](https://podscan.fm/docs/api) |
| [Get Team Alert](actions/get-team-alert.md) | `GET /teams/{team}/alerts/{alert}` | [docs](https://podscan.fm/docs/api) |
| [Get Team Alert Group](actions/get-team-alert-group.md) | `GET /teams/{team}/alert-groups/{group}` | [docs](https://podscan.fm/docs/api) |
| [Get Topic](actions/get-topic.md) | `GET /topics/{topicId}` | [docs](https://podscan.fm/docs/api) |
| [Get Topic Collection](actions/get-topic-collection.md) | `GET /topic-collections/{slug}` | [docs](https://podscan.fm/docs/api) |
| [Get Topic Demographics](actions/get-topic-demographics.md) | `GET /topics/{topicId}/demographics` | [docs](https://podscan.fm/docs/api) |
| [Get Trending Topics](actions/get-trending-topics.md) | `GET /topics/trending` | [docs](https://podscan.fm/docs/api) |
| [List Categories](actions/list-categories.md) | `GET /categories` | [docs](https://podscan.fm/docs/api) |
| [List Entity Appearances](actions/list-entity-appearances.md) | `GET /entities/{entityId}/appearances` | [docs](https://podscan.fm/docs/api) |
| [List Episode Entities](actions/list-episode-entities.md) | `GET /episodes/{episodeId}/entities` | [docs](https://podscan.fm/docs/api) |
| [List IAB Categories](actions/list-iab-categories.md) | `GET /iab-categories` | [docs](https://podscan.fm/docs/api) |
| [List Podcast Episodes](actions/list-podcast-episodes.md) | `GET /podcasts/{podcast}/episodes` | [docs](https://podscan.fm/docs/api) |
| [List Podcast Rankings](actions/list-podcast-rankings.md) | `GET /podcasts/rankings` | [docs](https://podscan.fm/docs/api) |
| [List Publisher Podcasts](actions/list-publisher-podcasts.md) | `GET /publishers/{publisherId}/podcasts` | [docs](https://podscan.fm/docs/api) |
| [List Recent Episodes](actions/list-recent-episodes.md) | `GET /episodes/recent` | [docs](https://podscan.fm/docs/api) |
| [List Related Podcasts](actions/list-related-podcasts.md) | `GET /podcasts/{podcast}/related_podcasts` | [docs](https://podscan.fm/docs/api) |
| [List Related Topics](actions/list-related-topics.md) | `GET /topics/{topicId}/related` | [docs](https://podscan.fm/docs/api) |
| [List Similar Entities](actions/list-similar-entities.md) | `GET /entities/{entityId}/similar` | [docs](https://podscan.fm/docs/api) |
| [List Sponsor Podcasts](actions/list-sponsor-podcasts.md) | `GET /sponsors/{sponsor}/podcasts` | [docs](https://podscan.fm/docs/api) |
| [List Sponsors](actions/list-sponsors.md) | `GET /sponsors` | [docs](https://podscan.fm/docs/api) |
| [List Team Alert Groups](actions/list-team-alert-groups.md) | `GET /teams/{team}/alert-groups` | [docs](https://podscan.fm/docs/api) |
| [List Team Alerts](actions/list-team-alerts.md) | `GET /teams/{team}/alerts` | [docs](https://podscan.fm/docs/api) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://podscan.fm/docs/api) |
| [List Topic Collections](actions/list-topic-collections.md) | `GET /topic-collections` | [docs](https://podscan.fm/docs/api) |
| [List Topic Episodes](actions/list-topic-episodes.md) | `GET /topics/{topicId}/episodes` | [docs](https://podscan.fm/docs/api) |
| [Search Entities](actions/search-entities.md) | `GET /entities/search` | [docs](https://podscan.fm/docs/api) |
| [Search Episodes](actions/search-episodes.md) | `GET /episodes/search` | [docs](https://podscan.fm/docs/api) |
| [Search Podcasts](actions/search-podcasts.md) | `GET /podcasts/search` | [docs](https://podscan.fm/docs/api) |
| [Search Publishers](actions/search-publishers.md) | `GET /publishers/search` | [docs](https://podscan.fm/docs/api) |
| [Search Sponsors](actions/search-sponsors.md) | `GET /sponsors/search` | [docs](https://podscan.fm/docs/api) |
| [Search Topics](actions/search-topics.md) | `GET /topics/search` | [docs](https://podscan.fm/docs/api) |
