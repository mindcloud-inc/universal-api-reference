# <img src="https://images.mindcloud.co/apps/icons/all-things-considered-podcast_1777563326167.png" alt="All Things Considered Podcast logo" width="28" height="28"> All Things Considered Podcast: Universal API

Read All Things Considered stories and audio links

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/allThingsConsideredPodcast/latest
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.npr.org/programs/all-things-considered
- **Vendor API docs:** https://www.npr.org/programs/all-things-considered/archive

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Stories](actions/list-stories.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/allThingsConsideredPodcast/latest/actions/list-stories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Archive Show

| Action | Method | Description |
| --- | --- | --- |
| [List Archive Shows](actions/list-archive-shows.md) | GET | Retrieves archived shows from All Things Considered Podcast. |
| [List Archive Shows By Date](actions/list-archive-shows-by-date.md) | GET | Retrieves archived shows by date from All Things Considered Podcast. |

### Audio Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Story Audio Metadata](actions/get-story-audio-metadata.md) | GET | Retrieves story audio metadata from All Things Considered Podcast. |

### Embedded Player

| Action | Method | Description |
| --- | --- | --- |
| [Get Embedded Player Metadata](actions/get-embedded-player-metadata.md) | GET | Retrieves embedded player metadata from All Things Considered Podcast. |

### Feed Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Feed Metadata](actions/get-feed-metadata.md) | GET | Retrieves feed metadata from All Things Considered Podcast. |

### Story

| Action | Method | Description |
| --- | --- | --- |
| [Get Story Details](actions/get-story-details.md) | GET | Retrieves story details from All Things Considered Podcast. |
| [List Stories](actions/list-stories.md) | GET | Retrieves recent stories from All Things Considered Podcast. |

### Transcript

| Action | Method | Description |
| --- | --- | --- |
| [Get Story Transcript](actions/get-story-transcript.md) | GET | Retrieves a story transcript from All Things Considered Podcast. |

