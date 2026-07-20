# <img src="https://images.mindcloud.co/apps/icons/active-network_1775567993778.png" alt="Active Network logo" width="28" height="28"> Active Network: Universal API

Find events, races, camps, and classes on ACTIVE

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/activeNetwork/latest
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.active.com
- **Vendor API docs:** https://developer.active.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Assets](actions/search-assets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activeNetwork/latest/actions/search-assets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Get Asset By Exact Name](actions/get-asset-by-exact-name.md) | GET | Retrieves an asset by exact name in Active Network. |
| [Get Asset By Guid](actions/get-asset-by-guid.md) | GET | Retrieves an asset by GUID in Active Network. |
| [Get Campground Details](actions/get-campground-details.md) | GET | Retrieves campground details in Active Network. |
| [Search Assets](actions/search-assets.md) | GET | Finds activity assets in Active Network. |
| [Search Campgrounds](actions/search-campgrounds.md) | GET | Finds campgrounds in Active Network. |
| [Search Campsites](actions/search-campsites.md) | GET | Finds campsites in Active Network. |
| [Search Kids Assets](actions/search-kids-assets.md) | GET | Finds kids activity assets in Active Network. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [List Activity Categories](actions/list-activity-categories.md) | GET | Finds activity categories in Active Network. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [List Activity Topics](actions/list-activity-topics.md) | GET | Finds activity topics in Active Network. |

