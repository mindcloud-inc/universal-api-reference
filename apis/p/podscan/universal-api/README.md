# <img src="https://images.mindcloud.co/apps/icons/podscan_1775847574219.png" alt="Podscan logo" width="28" height="28"> Podscan: Universal API

Search Podscan podcasts, episodes, mentions, entities, and team-managed alerts from the Podscan REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/podscan/latest
- **Actions:** 48
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://podscan.fm
- **Vendor API docs:** https://podscan.fm/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Teams](actions/list-teams.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podscan/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (48)

### Alert

| Action | Method | Description |
| --- | --- | --- |
| [Get Team Alert](actions/get-team-alert.md) | GET | Retrieves a team alert from Podscan. |
| [List Team Alerts](actions/list-team-alerts.md) | GET | Retrieves alerts for a team from Podscan. |

### Alert Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Team Alert Group](actions/get-team-alert-group.md) | GET | Retrieves a team alert group from Podscan. |
| [List Team Alert Groups](actions/list-team-alert-groups.md) | GET | Retrieves alert groups for a team from Podscan. |

### Analysis

| Action | Method | Description |
| --- | --- | --- |
| [Get Podcast Analysis](actions/get-podcast-analysis.md) | GET | Retrieves podcast analysis data from Podscan. |

### Appearance

| Action | Method | Description |
| --- | --- | --- |
| [List Entity Appearances](actions/list-entity-appearances.md) | GET | Retrieves entity appearance records from Podscan. |

### Brand Safety

| Action | Method | Description |
| --- | --- | --- |
| [Get Episode Brand Safety](actions/get-episode-brand-safety.md) | GET | Retrieves episode brand safety details from Podscan. |
| [Get Podcast Brand Safety](actions/get-podcast-brand-safety.md) | GET | Retrieves podcast brand safety details from Podscan. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [List Categories](actions/list-categories.md) | GET | Retrieves category records from your Podscan account. |

### Chart History

| Action | Method | Description |
| --- | --- | --- |
| [Get Podcast Chart History](actions/get-podcast-chart-history.md) | GET | Retrieves podcast chart history from Podscan. |

### Engagement

| Action | Method | Description |
| --- | --- | --- |
| [Get Episode Engagement](actions/get-episode-engagement.md) | GET | Retrieves episode engagement details from Podscan. |

### Entity

| Action | Method | Description |
| --- | --- | --- |
| [Get Entity](actions/get-entity.md) | GET | Retrieves an entity record from Podscan. |
| [List Episode Entities](actions/list-episode-entities.md) | GET | Retrieves entities mentioned in an episode from Podscan. |
| [List Similar Entities](actions/list-similar-entities.md) | GET | Retrieves similar entity matches from Podscan. |
| [Search Entities](actions/search-entities.md) | GET | Finds entities in Podscan by search text. |

### Episode

| Action | Method | Description |
| --- | --- | --- |
| [Get Episode](actions/get-episode.md) | GET | Retrieves an episode record from Podscan. |
| [Get Latest Podcast Episode](actions/get-latest-podcast-episode.md) | GET | Retrieves the latest podcast episode from Podscan. |
| [List Podcast Episodes](actions/list-podcast-episodes.md) | GET | Retrieves episodes for a podcast from Podscan. |
| [List Recent Episodes](actions/list-recent-episodes.md) | GET | Retrieves recent episode listings from Podscan. |
| [List Topic Episodes](actions/list-topic-episodes.md) | GET | Retrieves episodes for a topic from Podscan. |
| [Search Episodes](actions/search-episodes.md) | GET | Finds episodes in Podscan by search text. |

### Episode Demographics

| Action | Method | Description |
| --- | --- | --- |
| [Get Episode Demographics](actions/get-episode-demographics.md) | GET | Retrieves episode demographics data from Podscan. |

### Guest

| Action | Method | Description |
| --- | --- | --- |
| [Get Latest Podcast Guest](actions/get-latest-podcast-guest.md) | GET | Retrieves the latest podcast guest from Podscan. |

### Iab Category

| Action | Method | Description |
| --- | --- | --- |
| [Get IAB Category](actions/get-iab-category.md) | GET | Retrieves an IAB category from Podscan. |
| [List IAB Categories](actions/list-iab-categories.md) | GET | Retrieves IAB category records from Podscan. |

### Podcast

| Action | Method | Description |
| --- | --- | --- |
| [Get Podcast](actions/get-podcast.md) | GET | Retrieves a podcast record from Podscan. |
| [List Publisher Podcasts](actions/list-publisher-podcasts.md) | GET | Retrieves podcasts for a publisher from Podscan. |
| [List Related Podcasts](actions/list-related-podcasts.md) | GET | Retrieves related podcast recommendations from Podscan. |
| [List Sponsor Podcasts](actions/list-sponsor-podcasts.md) | GET | Retrieves podcasts for a sponsor from Podscan. |
| [Search Podcasts](actions/search-podcasts.md) | GET | Finds podcasts in Podscan by search text. |

### Podcast Demographics

| Action | Method | Description |
| --- | --- | --- |
| [Get Podcast Demographics](actions/get-podcast-demographics.md) | GET | Retrieves podcast demographics data from Podscan. |

### Podcast Discovery

| Action | Method | Description |
| --- | --- | --- |
| [Discover Similar Podcasts](actions/discover-similar-podcasts.md) | GET | Retrieves similar podcast recommendations from Podscan. |

### Podcast Ranking

| Action | Method | Description |
| --- | --- | --- |
| [List Podcast Rankings](actions/list-podcast-rankings.md) | GET | Retrieves podcast ranking data from Podscan. |

### Publisher

| Action | Method | Description |
| --- | --- | --- |
| [Get Publisher](actions/get-publisher.md) | GET | Retrieves a publisher record from Podscan. |
| [Search Publishers](actions/search-publishers.md) | GET | Finds publishers in Podscan by search text. |

### Sponsor

| Action | Method | Description |
| --- | --- | --- |
| [Get Latest Podcast Sponsor](actions/get-latest-podcast-sponsor.md) | GET | Retrieves the latest podcast sponsor from Podscan. |
| [Get Sponsor](actions/get-sponsor.md) | GET | Retrieves a sponsor record from Podscan. |
| [List Sponsors](actions/list-sponsors.md) | GET | Retrieves sponsor records from your Podscan account. |
| [Search Sponsors](actions/search-sponsors.md) | GET | Finds sponsors in Podscan by search text. |

### Sponsor Trend

| Action | Method | Description |
| --- | --- | --- |
| [Get Sponsor Trend](actions/get-sponsor-trend.md) | GET | Retrieves sponsor trend data from Podscan. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET | Retrieves team records from your Podscan account. |

### Topic

| Action | Method | Description |
| --- | --- | --- |
| [Get Topic](actions/get-topic.md) | GET | Retrieves a topic record from Podscan. |
| [Get Trending Topics](actions/get-trending-topics.md) | GET | Retrieves trending topic results from Podscan. |
| [List Related Topics](actions/list-related-topics.md) | GET | Retrieves related topic matches from Podscan. |
| [Search Topics](actions/search-topics.md) | GET | Finds topics in Podscan by search text. |

### Topic Collection

| Action | Method | Description |
| --- | --- | --- |
| [Get Topic Collection](actions/get-topic-collection.md) | GET | Retrieves a topic collection from Podscan. |
| [List Topic Collections](actions/list-topic-collections.md) | GET | Retrieves topic collection records from Podscan. |

### Topic Demographics

| Action | Method | Description |
| --- | --- | --- |
| [Get Topic Demographics](actions/get-topic-demographics.md) | GET | Retrieves topic demographics data from Podscan. |

