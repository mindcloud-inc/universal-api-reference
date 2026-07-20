# <img src="https://images.mindcloud.co/apps/icons/simplecast-icon_1776710136098.png" alt="Simplecast logo" width="28" height="28"> Simplecast: Universal API

Simplecast is a podcast hosting, distribution, and analytics platform. This app lets users manage Simplecast podcast resources, episodes, catalog metadata, and analytics through the Simplecast API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/simplecast/latest
- **Actions:** 62
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.simplecast.com
- **Vendor API docs:** https://apidocs.simplecast.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Podcasts](actions/list-podcasts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/list-podcasts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (62)

### Analytics Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Analytics Summary](actions/get-analytics-summary.md) | GET | Retrieves analytics summary data from Simplecast. |

### Application Analytics

| Action | Method | Description |
| --- | --- | --- |
| [List Application Analytics](actions/list-application-analytics.md) | GET | Retrieves application analytics from Simplecast. |

### Author

| Action | Method | Description |
| --- | --- | --- |
| [Get Author](actions/get-author.md) | GET | Retrieves an author from Simplecast by ID. |

### Browser Analytics

| Action | Method | Description |
| --- | --- | --- |
| [List Browser Analytics](actions/list-browser-analytics.md) | GET | Retrieves browser analytics from Simplecast. |

### Campaign Analytics

| Action | Method | Description |
| --- | --- | --- |
| [List Campaign Analytics](actions/list-campaign-analytics.md) | GET | Retrieves campaign analytics from Simplecast. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [List Categories](actions/list-categories.md) | GET | Retrieves categories from Simplecast. |

### Device Analytics

| Action | Method | Description |
| --- | --- | --- |
| [List Device Analytics](actions/list-device-analytics.md) | GET | Retrieves device analytics from Simplecast. |

### Device Class Analytics

| Action | Method | Description |
| --- | --- | --- |
| [List Device Class Analytics](actions/list-device-class-analytics.md) | GET | Retrieves device class analytics from Simplecast. |

### Distribution Channel

| Action | Method | Description |
| --- | --- | --- |
| [Get Distribution Channel](actions/get-distribution-channel.md) | GET | Retrieves a distribution channel from Simplecast by ID. |
| [List Distribution Channels](actions/list-distribution-channels.md) | GET | Retrieves distribution channels from Simplecast. |

### Download Analytics

| Action | Method | Description |
| --- | --- | --- |
| [List Download Analytics](actions/list-download-analytics.md) | GET | Retrieves download analytics from Simplecast. |

### Embed Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Embed Analytics](actions/get-embed-analytics.md) | GET | Retrieves embed analytics from Simplecast. |

### Embed Completion Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Embed Average Completion](actions/get-embed-average-completion.md) | GET | Retrieves embed average completion analytics from Simplecast. |

### Embed Episode Analytics

| Action | Method | Description |
| --- | --- | --- |
| [List Embed Episode Analytics](actions/list-embed-episode-analytics.md) | GET | Retrieves embed episode analytics from Simplecast. |

### Embed Heatmap Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Embed Heatmap Analytics](actions/get-embed-heatmap-analytics.md) | GET | Retrieves embed heatmap analytics from Simplecast. |

### Embed Listen Analytics

| Action | Method | Description |
| --- | --- | --- |
| [List Embed Listen Analytics](actions/list-embed-listen-analytics.md) | GET | Retrieves embed listen analytics from Simplecast. |

### Embed Location Analytics

| Action | Method | Description |
| --- | --- | --- |
| [List Embed Location Analytics](actions/list-embed-location-analytics.md) | GET | Retrieves embed location analytics from Simplecast. |

### Embed Speed Analytics

| Action | Method | Description |
| --- | --- | --- |
| [List Embed Speed Analytics](actions/list-embed-speed-analytics.md) | GET | Retrieves embed playback speed analytics from Simplecast. |

### Episode

| Action | Method | Description |
| --- | --- | --- |
| [Get Episode](actions/get-episode.md) | GET | Retrieves an episode from Simplecast by ID. |
| [List Podcast Episodes](actions/list-podcast-episodes.md) | GET | Retrieves episodes for a podcast from Simplecast. |

### Episode Analytics

| Action | Method | Description |
| --- | --- | --- |
| [List Episode Analytics](actions/list-episode-analytics.md) | GET | Retrieves episode analytics from Simplecast. |

### Episode Audio

| Action | Method | Description |
| --- | --- | --- |
| [Upload Episode Audio](actions/upload-episode-audio.md) | POST | Uploads episode audio to Simplecast. |

### Episode Author

| Action | Method | Description |
| --- | --- | --- |
| [List Episode Authors](actions/list-episode-authors.md) | GET | Retrieves authors for an episode from Simplecast. |

### Episode Average Download Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Average Episode Downloads](actions/get-average-episode-downloads.md) | GET | Retrieves average episode downloads from Simplecast. |

### Episode Hours Listened Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Episode Hours Listened](actions/get-episode-hours-listened.md) | GET | Retrieves episode hours listened from Simplecast. |

### Episode Keyword

| Action | Method | Description |
| --- | --- | --- |
| [Get Episode Keyword](actions/get-episode-keyword.md) | GET | Retrieves an episode keyword from Simplecast by ID. |
| [List Episode Keywords](actions/list-episode-keywords.md) | GET | Retrieves keywords for an episode from Simplecast. |

### Episode Listener Analytics

| Action | Method | Description |
| --- | --- | --- |
| [List Episode Listener Analytics](actions/list-episode-listener-analytics.md) | GET | Retrieves episode listener analytics from Simplecast. |

### Episode Marker

| Action | Method | Description |
| --- | --- | --- |
| [Get Episode Marker](actions/get-episode-marker.md) | GET | Retrieves an episode marker from Simplecast by ID. |
| [List Episode Markers](actions/list-episode-markers.md) | GET | Retrieves markers for an episode from Simplecast. |

### Keyword

| Action | Method | Description |
| --- | --- | --- |
| [Get Keyword](actions/get-keyword.md) | GET | Retrieves a keyword from Simplecast by ID. |

### Link

| Action | Method | Description |
| --- | --- | --- |
| [Get Link](actions/get-link.md) | GET | Retrieves a link from Simplecast by ID. |

### Listener Analytics

| Action | Method | Description |
| --- | --- | --- |
| [List Listener Analytics](actions/list-listener-analytics.md) | GET | Retrieves listener analytics from Simplecast. |

### Listening Method Analytics

| Action | Method | Description |
| --- | --- | --- |
| [List Listening Method Analytics](actions/list-listening-method-analytics.md) | GET | Retrieves listening method analytics from Simplecast. |

### Location Analytics

| Action | Method | Description |
| --- | --- | --- |
| [List Location Analytics](actions/list-location-analytics.md) | GET | Retrieves location analytics from Simplecast. |

### Network Type Analytics

| Action | Method | Description |
| --- | --- | --- |
| [List Network Type Analytics](actions/list-network-type-analytics.md) | GET | Retrieves network type analytics from Simplecast. |

### Oembed

| Action | Method | Description |
| --- | --- | --- |
| [Get OEmbed](actions/get-oembed.md) | GET | Retrieves oEmbed data from Simplecast. |

### Operating System Analytics

| Action | Method | Description |
| --- | --- | --- |
| [List Operating System Analytics](actions/list-operating-system-analytics.md) | GET | Retrieves operating system analytics from Simplecast. |

### Podcast

| Action | Method | Description |
| --- | --- | --- |
| [Get Podcast](actions/get-podcast.md) | GET | Retrieves a podcast from Simplecast by ID. |
| [List Podcasts](actions/list-podcasts.md) | GET | Retrieves podcasts from Simplecast. |

### Podcast Author

| Action | Method | Description |
| --- | --- | --- |
| [List Podcast Authors](actions/list-podcast-authors.md) | GET | Retrieves authors for a podcast from Simplecast. |

### Podcast Category

| Action | Method | Description |
| --- | --- | --- |
| [Get Podcast Category](actions/get-podcast-category.md) | GET | Retrieves a podcast category from Simplecast by ID. |
| [List Podcast Categories](actions/list-podcast-categories.md) | GET | Retrieves categories for a podcast from Simplecast. |

### Podcast Distribution Channel

| Action | Method | Description |
| --- | --- | --- |
| [Get Podcast Distribution Channel](actions/get-podcast-distribution-channel.md) | GET | Retrieves a podcast distribution channel from Simplecast by ID. |
| [List Podcast Distribution Channels](actions/list-podcast-distribution-channels.md) | GET | Retrieves distribution channels for a podcast from Simplecast. |

### Podcast Keyword

| Action | Method | Description |
| --- | --- | --- |
| [Get Podcast Keyword](actions/get-podcast-keyword.md) | GET | Retrieves a podcast keyword from Simplecast by ID. |
| [List Podcast Keywords](actions/list-podcast-keywords.md) | GET | Retrieves keywords for a podcast from Simplecast. |

### Podcast Listener Analytics

| Action | Method | Description |
| --- | --- | --- |
| [List Podcast Listener Analytics](actions/list-podcast-listener-analytics.md) | GET | Retrieves podcast listener analytics from Simplecast. |

### Podcast Rss Feed

| Action | Method | Description |
| --- | --- | --- |
| [Get Podcast RSS](actions/get-podcast-rss.md) | GET | Retrieves a podcast RSS feed from Simplecast. |

### Podcast Subcategory

| Action | Method | Description |
| --- | --- | --- |
| [Get Podcast Subcategory](actions/get-podcast-subcategory.md) | GET | Retrieves a podcast subcategory from Simplecast by ID. |
| [List Podcast Subcategories](actions/list-podcast-subcategories.md) | GET | Retrieves podcast subcategories from Simplecast. |

### Provider Analytics

| Action | Method | Description |
| --- | --- | --- |
| [List Provider Analytics](actions/list-provider-analytics.md) | GET | Retrieves provider analytics from Simplecast. |

### Recent Listener Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Last 7 Days Listeners](actions/get-last-7-days-listeners.md) | GET | Retrieves last 7 days listener analytics from Simplecast. |

### Season

| Action | Method | Description |
| --- | --- | --- |
| [Get Season](actions/get-season.md) | GET | Retrieves a season from Simplecast by ID. |
| [List Podcast Seasons](actions/list-podcast-seasons.md) | GET | Retrieves seasons for a podcast from Simplecast. |

### Season Episode

| Action | Method | Description |
| --- | --- | --- |
| [List Season Episodes](actions/list-season-episodes.md) | GET | Retrieves episodes for a season from Simplecast. |

### Technology Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Technology Analytics](actions/get-technology-analytics.md) | GET | Retrieves technology analytics from Simplecast. |

### Time Of Week Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Time Of Week Analytics](actions/get-time-of-week-analytics.md) | GET | Retrieves time-of-week analytics from Simplecast. |

### Timezone

| Action | Method | Description |
| --- | --- | --- |
| [List Timezones](actions/list-timezones.md) | GET | Retrieves timezones from Simplecast. |

### Top Episode Analytics

| Action | Method | Description |
| --- | --- | --- |
| [List Top Episodes](actions/list-top-episodes.md) | GET | Retrieves top episodes from Simplecast analytics. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Simplecast. |

### Web Player Analytics

| Action | Method | Description |
| --- | --- | --- |
| [List Web Player Analytics](actions/list-web-player-analytics.md) | GET | Retrieves web player analytics from Simplecast. |

