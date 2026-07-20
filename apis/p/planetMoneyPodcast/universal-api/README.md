# <img src="https://images.mindcloud.co/apps/icons/planet-money-podcast_1776452428130.png" alt="Planet Money Podcast logo" width="28" height="28"> Planet Money Podcast: Universal API

Read the public Planet Money podcast feed, archive pages, episode pages, transcripts, and embed pages.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/planetMoneyPodcast/latest
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.npr.org/podcasts/510289/planet-money
- **Vendor API docs:** https://www.npr.org/podcasts/510289/planet-money

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get About Page](actions/get-about-page.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planetMoneyPodcast/latest/actions/get-about-page?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Get About Page](actions/get-about-page.md) | GET | Retrieves NPR's About Planet Money page. |
| [Get Episode Embed Player](actions/get-episode-embed-player.md) | GET | Retrieves the NPR embed player page for a Planet Money episode. |
| [Get Episode Transcript](actions/get-episode-transcript.md) | GET | Retrieves a Planet Money episode transcript page from NPR. |
| [Get Podcast Episode Page](actions/get-podcast-episode-page.md) | GET | Retrieves a Planet Money episode page from NPR. |
| [Get Podcast Show Page](actions/get-podcast-show-page.md) | GET | Retrieves the Planet Money show page from NPR. |
| [List Podcast Archive](actions/list-podcast-archive.md) | GET | Retrieves older Planet Money episode listings from NPR. |
| [List Recent Episodes](actions/list-recent-episodes.md) | GET | Retrieves the latest Planet Money episodes from the NPR RSS feed. |

