# <img src="https://images.mindcloud.co/apps/icons/pexels-icon_1778274409113.png" alt="Pexels logo" width="28" height="28"> Pexels: Universal API

Search, browse, and retrieve Pexels stock photos, videos, and collections from the official Pexels API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pexels/latest
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.pexels.com
- **Vendor API docs:** https://www.pexels.com/api/documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Photos](actions/search-photos.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pexels/latest/actions/search-photos?connectionId=$CONNECTION_ID&limit=25&offset=0&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [List Featured Collections](actions/list-featured-collections.md) | GET | Retrieves featured collections available in Pexels. |
| [List My Collections](actions/list-my-collections.md) | GET | Retrieves your saved collections from Pexels. |

### Collection Media

| Action | Method | Description |
| --- | --- | --- |
| [List Collection Media](actions/list-collection-media.md) | GET | Retrieves media from a Pexels collection. |

### Photo

| Action | Method | Description |
| --- | --- | --- |
| [Get Photo](actions/get-photo.md) | GET | Retrieves a photo from Pexels by ID. |
| [List Curated Photos](actions/list-curated-photos.md) | GET | Retrieves curated photo results from Pexels. |
| [Search Photos](actions/search-photos.md) | GET | Finds photos in Pexels by search query. |

### Video

| Action | Method | Description |
| --- | --- | --- |
| [Get Video](actions/get-video.md) | GET | Retrieves a video from Pexels by ID. |
| [List Popular Videos](actions/list-popular-videos.md) | GET | Retrieves popular video results from Pexels. |
| [Search Videos](actions/search-videos.md) | GET | Finds videos in Pexels by search query. |

