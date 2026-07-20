# <img src="https://images.mindcloud.co/apps/icons/vooplayer_1775595851022.png" alt="Vooplayer logo" width="28" height="28"> Vooplayer: Universal API

Create, manage, and analyze Spotlightr/vooPlayer videos, projects, player settings, domains, students, and assets.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/vooplayer/latest
- **Category:** Content & Files / Storage
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://spotlightr.com
- **Vendor API docs:** https://app.spotlightr.com/docs/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Vooplayer. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from your Vooplayer account. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Global Search](actions/global-search.md) | GET | Finds matching records across your Vooplayer account. |

### Video

| Action | Method | Description |
| --- | --- | --- |
| [Create Video](actions/create-video.md) | POST | Creates a new video in Vooplayer. |
| [Delete Videos](actions/delete-videos.md) | DELETE | Deletes one or more videos from Vooplayer. |
| [Get Video Metrics](actions/get-video-metrics.md) | GET | Retrieves video analytics data from Vooplayer. |
| [List Videos](actions/list-videos.md) | GET | Retrieves videos from Vooplayer by video or project. |
| [Set Video Source](actions/set-video-source.md) | PUT | Updates a video's source URL in Vooplayer. |
| [Update Video Player Settings](actions/update-video-player-settings.md) | PUT | Updates video player settings in Vooplayer. |

### Video View

| Action | Method | Description |
| --- | --- | --- |
| [Get Video Views](actions/get-video-views.md) | GET | Retrieves video view records from Vooplayer. |

### Whitelisted Domain

| Action | Method | Description |
| --- | --- | --- |
| [Add Whitelisted Domain](actions/add-whitelisted-domain.md) | POST | Creates a whitelisted domain in Vooplayer. |
| [List Whitelisted Domains](actions/list-whitelisted-domains.md) | GET | Retrieves whitelisted domains from your Vooplayer account. |

