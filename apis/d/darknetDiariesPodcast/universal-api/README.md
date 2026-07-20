# <img src="https://images.mindcloud.co/apps/icons/darknet_1776442906989.jpeg" alt="Darknet Diaries Podcast logo" width="28" height="28"> Darknet Diaries Podcast: Universal API

Browse Darknet Diaries episodes and podcast metadata

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/darknetDiariesPodcast/latest
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://darknetdiaries.com
- **Vendor API docs:** https://darknetdiaries.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Episode By GUID](actions/get-episode-by-guid.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/darknetDiariesPodcast/latest/actions/get-episode-by-guid?connectionId=$CONNECTION_ID&guid=prx_7057_cb64ead7-d1f0-41c4-885c-84ce8b3e42d9" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Episode

| Action | Method | Description |
| --- | --- | --- |
| [Get Episode By GUID](actions/get-episode-by-guid.md) | GET | Retrieves a podcast episode by GUID from Darknet Diaries Podcast. |
| [Get Episode By Number](actions/get-episode-by-number.md) | GET | Retrieves a podcast episode by episode number from Darknet Diaries Podcast. |
| [Get Latest Episode](actions/get-latest-episode.md) | GET | Retrieves the latest podcast episode from Darknet Diaries Podcast. |
| [List Clean Episodes](actions/list-clean-episodes.md) | GET | Retrieves clean podcast episodes from Darknet Diaries Podcast. |
| [List Episodes](actions/list-episodes.md) | GET | Retrieves podcast episodes from Darknet Diaries Podcast. |
| [List Episodes By Date Range](actions/list-episodes-by-date-range.md) | GET | Retrieves podcast episodes in a date range from Darknet Diaries Podcast. |
| [List Episodes Published After](actions/list-episodes-published-after.md) | GET | Retrieves podcast episodes published after a date from Darknet Diaries Podcast. |
| [List Episodes Published Before](actions/list-episodes-published-before.md) | GET | Retrieves podcast episodes published before a date from Darknet Diaries Podcast. |
| [List Episodes With Transcripts](actions/list-episodes-with-transcripts.md) | GET | Retrieves podcast episodes with transcripts from Darknet Diaries Podcast. |
| [List Episodes Without Transcripts](actions/list-episodes-without-transcripts.md) | GET | Retrieves podcast episodes without transcripts from Darknet Diaries Podcast. |
| [List Explicit Episodes](actions/list-explicit-episodes.md) | GET | Retrieves explicit podcast episodes from Darknet Diaries Podcast. |
| [List Recent Episodes](actions/list-recent-episodes.md) | GET | Retrieves recent podcast episodes from Darknet Diaries Podcast. |
| [Search Episodes By Summary](actions/search-episodes-by-summary.md) | GET | Finds podcast episodes in Darknet Diaries Podcast by summary text. |
| [Search Episodes By Title](actions/search-episodes-by-title.md) | GET | Finds podcast episodes in Darknet Diaries Podcast by title. |

### Episode Artwork

| Action | Method | Description |
| --- | --- | --- |
| [List Episode Artwork](actions/list-episode-artwork.md) | GET | Retrieves episode artwork from Darknet Diaries Podcast. |

### Episode Audio Asset

| Action | Method | Description |
| --- | --- | --- |
| [List Episode Audio Assets](actions/list-episode-audio-assets.md) | GET | Retrieves episode audio assets from Darknet Diaries Podcast. |

### Episode Transcript

| Action | Method | Description |
| --- | --- | --- |
| [List Episode Transcripts](actions/list-episode-transcripts.md) | GET | Retrieves episode transcripts from Darknet Diaries Podcast. |

### Podcast

| Action | Method | Description |
| --- | --- | --- |
| [Get Podcast Metadata](actions/get-podcast-metadata.md) | GET | Retrieves podcast metadata from Darknet Diaries Podcast. |

### Podcast Artwork

| Action | Method | Description |
| --- | --- | --- |
| [Get Podcast Artwork](actions/get-podcast-artwork.md) | GET | Retrieves podcast artwork from Darknet Diaries Podcast. |

### Podcast Feed

| Action | Method | Description |
| --- | --- | --- |
| [Get Podcast Feed Information](actions/get-podcast-feed-information.md) | GET | Retrieves podcast feed information from Darknet Diaries Podcast. |

