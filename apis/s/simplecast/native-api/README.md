# Simplecast: Native API Reference

A consolidated summary of Simplecast's API configuration and 62 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.simplecast.com
- **API base URL:** `https://api.simplecast.com`

## Authentication

### API token

Authenticate to Simplecast with a Private Apps API token sent as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.simplecast.com/hc/en-us/articles/21953603587613-Simplecast-API)

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (62 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Analytics Summary](actions/get-analytics-summary.md) | `GET /analytics` | [docs](https://apidocs.simplecast.com/) |
| [Get Author](actions/get-author.md) | `GET /authors/:author_id` | [docs](https://apidocs.simplecast.com/) |
| [Get Average Episode Downloads](actions/get-average-episode-downloads.md) | `GET /analytics/episodes/average_downloads` | [docs](https://apidocs.simplecast.com/) |
| [Get Current User](actions/get-current-user.md) | `GET /current_user` | [docs](https://apidocs.simplecast.com/) |
| [Get Distribution Channel](actions/get-distribution-channel.md) | `GET /distribution_channels/:distribution_channel_id` | [docs](https://apidocs.simplecast.com/) |
| [Get Embed Analytics](actions/get-embed-analytics.md) | `GET /analytics/embed` | [docs](https://apidocs.simplecast.com/) |
| [Get Embed Average Completion](actions/get-embed-average-completion.md) | `GET /analytics/embed/avg_completion` | [docs](https://apidocs.simplecast.com/) |
| [Get Embed Heatmap Analytics](actions/get-embed-heatmap-analytics.md) | `GET /analytics/embed/heatmap` | [docs](https://apidocs.simplecast.com/) |
| [Get Episode](actions/get-episode.md) | `GET /episodes/:episode_id` | [docs](https://apidocs.simplecast.com/) |
| [Get Episode Hours Listened](actions/get-episode-hours-listened.md) | `GET /analytics/episodes/hours_listened` | [docs](https://apidocs.simplecast.com/) |
| [Get Episode Keyword](actions/get-episode-keyword.md) | `GET /episodes/:episode_id/keywords/:keyword_id` | [docs](https://apidocs.simplecast.com/) |
| [Get Episode Marker](actions/get-episode-marker.md) | `GET /episodes/:episode_id/markers/:marker_id` | [docs](https://apidocs.simplecast.com/) |
| [Get Keyword](actions/get-keyword.md) | `GET /keywords/:keyword_id` | [docs](https://apidocs.simplecast.com/) |
| [Get Last 7 Days Listeners](actions/get-last-7-days-listeners.md) | `GET /analytics/listeners/last_7` | [docs](https://apidocs.simplecast.com/) |
| [Get Link](actions/get-link.md) | `GET /links/:link_id` | [docs](https://apidocs.simplecast.com/) |
| [Get OEmbed](actions/get-oembed.md) | `GET /oembed` | [docs](https://apidocs.simplecast.com/) |
| [Get Podcast](actions/get-podcast.md) | `GET /podcasts/:podcast_id` | [docs](https://apidocs.simplecast.com/) |
| [Get Podcast Category](actions/get-podcast-category.md) | `GET /podcasts/:podcast_id/categories/:category_id` | [docs](https://apidocs.simplecast.com/) |
| [Get Podcast Distribution Channel](actions/get-podcast-distribution-channel.md) | `GET /podcasts/:podcast_id/distribution_channels/:distribution_channel_id` | [docs](https://apidocs.simplecast.com/) |
| [Get Podcast Keyword](actions/get-podcast-keyword.md) | `GET /podcasts/:podcast_id/keywords/:keyword_id` | [docs](https://apidocs.simplecast.com/) |
| [Get Podcast RSS](actions/get-podcast-rss.md) | `GET /podcasts/:podcast_id/rss` | [docs](https://apidocs.simplecast.com/) |
| [Get Podcast Subcategory](actions/get-podcast-subcategory.md) | `GET /podcasts/:podcast_id/categories/:category_id/subcategories/:subcategory_id` | [docs](https://apidocs.simplecast.com/) |
| [Get Season](actions/get-season.md) | `GET /seasons/:season_id` | [docs](https://apidocs.simplecast.com/) |
| [Get Technology Analytics](actions/get-technology-analytics.md) | `GET /analytics/technology` | [docs](https://apidocs.simplecast.com/) |
| [Get Time Of Week Analytics](actions/get-time-of-week-analytics.md) | `GET /analytics/time_of_week` | [docs](https://apidocs.simplecast.com/) |
| [List Application Analytics](actions/list-application-analytics.md) | `GET /analytics/technology/applications` | [docs](https://apidocs.simplecast.com/) |
| [List Browser Analytics](actions/list-browser-analytics.md) | `GET /analytics/technology/browsers` | [docs](https://apidocs.simplecast.com/) |
| [List Campaign Analytics](actions/list-campaign-analytics.md) | `GET /analytics/campaigns` | [docs](https://apidocs.simplecast.com/) |
| [List Categories](actions/list-categories.md) | `GET /categories` | [docs](https://apidocs.simplecast.com/) |
| [List Device Analytics](actions/list-device-analytics.md) | `GET /analytics/technology/devices` | [docs](https://apidocs.simplecast.com/) |
| [List Device Class Analytics](actions/list-device-class-analytics.md) | `GET /analytics/technology/device_class` | [docs](https://apidocs.simplecast.com/) |
| [List Distribution Channels](actions/list-distribution-channels.md) | `GET /distribution_channels` | [docs](https://apidocs.simplecast.com/) |
| [List Download Analytics](actions/list-download-analytics.md) | `GET /analytics/downloads` | [docs](https://apidocs.simplecast.com/) |
| [List Embed Episode Analytics](actions/list-embed-episode-analytics.md) | `GET /analytics/embed/episodes` | [docs](https://apidocs.simplecast.com/) |
| [List Embed Listen Analytics](actions/list-embed-listen-analytics.md) | `GET /analytics/embed/listens` | [docs](https://apidocs.simplecast.com/) |
| [List Embed Location Analytics](actions/list-embed-location-analytics.md) | `GET /analytics/embed/locations` | [docs](https://apidocs.simplecast.com/) |
| [List Embed Speed Analytics](actions/list-embed-speed-analytics.md) | `GET /analytics/embed/speeds` | [docs](https://apidocs.simplecast.com/) |
| [List Episode Analytics](actions/list-episode-analytics.md) | `GET /analytics/episodes` | [docs](https://apidocs.simplecast.com/) |
| [List Episode Authors](actions/list-episode-authors.md) | `GET /episodes/:episode_id/authors` | [docs](https://apidocs.simplecast.com/) |
| [List Episode Keywords](actions/list-episode-keywords.md) | `GET /episodes/:episode_id/keywords` | [docs](https://apidocs.simplecast.com/) |
| [List Episode Listener Analytics](actions/list-episode-listener-analytics.md) | `GET /analytics/episodes/listeners` | [docs](https://apidocs.simplecast.com/) |
| [List Episode Markers](actions/list-episode-markers.md) | `GET /episodes/:episode_id/markers` | [docs](https://apidocs.simplecast.com/) |
| [List Listener Analytics](actions/list-listener-analytics.md) | `GET /analytics/listeners` | [docs](https://apidocs.simplecast.com/) |
| [List Listening Method Analytics](actions/list-listening-method-analytics.md) | `GET /analytics/technology/listening_methods` | [docs](https://apidocs.simplecast.com/) |
| [List Location Analytics](actions/list-location-analytics.md) | `GET /analytics/location` | [docs](https://apidocs.simplecast.com/) |
| [List Network Type Analytics](actions/list-network-type-analytics.md) | `GET /analytics/technology/network_types` | [docs](https://apidocs.simplecast.com/) |
| [List Operating System Analytics](actions/list-operating-system-analytics.md) | `GET /analytics/technology/operating_systems` | [docs](https://apidocs.simplecast.com/) |
| [List Podcast Authors](actions/list-podcast-authors.md) | `GET /podcasts/:podcast_id/authors` | [docs](https://apidocs.simplecast.com/) |
| [List Podcast Categories](actions/list-podcast-categories.md) | `GET /podcasts/:podcast_id/categories` | [docs](https://apidocs.simplecast.com/) |
| [List Podcast Distribution Channels](actions/list-podcast-distribution-channels.md) | `GET /podcasts/:podcast_id/distribution_channels` | [docs](https://apidocs.simplecast.com/) |
| [List Podcast Episodes](actions/list-podcast-episodes.md) | `GET /podcasts/:podcast_id/episodes` | [docs](https://apidocs.simplecast.com/) |
| [List Podcast Keywords](actions/list-podcast-keywords.md) | `GET /podcasts/:podcast_id/keywords` | [docs](https://apidocs.simplecast.com/) |
| [List Podcast Listener Analytics](actions/list-podcast-listener-analytics.md) | `GET /analytics/podcasts/listeners` | [docs](https://apidocs.simplecast.com/) |
| [List Podcast Seasons](actions/list-podcast-seasons.md) | `GET /podcasts/:podcast_id/seasons` | [docs](https://apidocs.simplecast.com/) |
| [List Podcast Subcategories](actions/list-podcast-subcategories.md) | `GET /podcasts/:podcast_id/categories/:category_id/subcategories` | [docs](https://apidocs.simplecast.com/) |
| [List Podcasts](actions/list-podcasts.md) | `GET /podcasts` | [docs](https://apidocs.simplecast.com/) |
| [List Provider Analytics](actions/list-provider-analytics.md) | `GET /analytics/technology/providers` | [docs](https://apidocs.simplecast.com/) |
| [List Season Episodes](actions/list-season-episodes.md) | `GET /seasons/:season_id/episodes` | [docs](https://apidocs.simplecast.com/) |
| [List Timezones](actions/list-timezones.md) | `GET /timezones` | [docs](https://apidocs.simplecast.com/) |
| [List Top Episodes](actions/list-top-episodes.md) | `GET /analytics/episodes/top_10` | [docs](https://apidocs.simplecast.com/) |
| [List Web Player Analytics](actions/list-web-player-analytics.md) | `GET /analytics/technology/web_players` | [docs](https://apidocs.simplecast.com/) |
| [Upload Episode Audio](actions/upload-episode-audio.md) | `POST /episodes/:episode_id/audio` | [docs](https://apidocs.simplecast.com/) |
