# <img src="https://images.mindcloud.co/apps/icons/shortio_1773254453145.png" alt="Short.io logo" width="28" height="28"> Short.io: Universal API

Create branded short links and track click analytics

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/shortio/latest
- **Category:** Marketing
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://short.io
- **Vendor API docs:** https://developers.short.io/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Domains](actions/list-domains.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shortio/latest/actions/list-domains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [Create Domain](actions/create-domain.md) | POST | Creates a new domain in Short.io. |
| [Get Domain](actions/get-domain.md) | GET | Retrieves domain details from Short.io by ID. |
| [List Domains](actions/list-domains.md) | GET | Retrieves domains from Short.io. |

### Domain Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Domain Statistics](actions/get-domain-statistics.md) | GET | Retrieves domain statistics from Short.io. |

### Link

| Action | Method | Description |
| --- | --- | --- |
| [Add Single Tag to Links in Bulk](actions/add-single-tag-to-links-in-bulk.md) | PUT | Adds a tag to links in bulk in Short.io. |
| [Archive Link](actions/archive-link.md) | PUT | Archives an existing link in Short.io. |
| [Archive Links in Bulk](actions/archive-links-in-bulk.md) | PUT | Archives links in bulk in Short.io. |
| [Create Link](actions/create-link.md) | POST | Creates a new link in Short.io. |
| [Delete Link](actions/delete-link.md) | DELETE | Deletes an existing link from Short.io. |
| [Delete Links in Bulk](actions/delete-links-in-bulk.md) | DELETE | Deletes links in bulk from Short.io. |
| [Get Link](actions/get-link.md) | GET | Retrieves link details from Short.io by ID. |
| [Get Link by Path](actions/get-link-by-path.md) | GET | Retrieves link details from Short.io by path. |
| [List Links](actions/list-links.md) | GET | Retrieves links from Short.io. |
| [List Links by Original URL](actions/list-links-by-original-url.md) | GET | Finds links in Short.io by original URL. |
| [Unarchive Link](actions/unarchive-link.md) | PUT | Unarchives an existing link in Short.io. |
| [Unarchive Links in Bulk](actions/unarchive-links-in-bulk.md) | PUT | Unarchives links in bulk in Short.io. |
| [Update Link](actions/update-link.md) | PUT | Updates an existing link in Short.io. |

### Link Clicks

| Action | Method | Description |
| --- | --- | --- |
| [Get Link Clicks By IDs](actions/get-link-clicks-by-i-ds.md) | GET | Retrieves link clicks from Short.io by link IDs. |
| [Get Link Clicks By Paths](actions/get-link-clicks-by-paths.md) | GET | Retrieves link clicks from Short.io by paths. |

### Link Region

| Action | Method | Description |
| --- | --- | --- |
| [Get Link Regions](actions/get-link-regions.md) | GET | Retrieves link regions from Short.io. |

### Link Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Link Statistics](actions/get-link-statistics.md) | GET | Retrieves link statistics from Short.io. |

