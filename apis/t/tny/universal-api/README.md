# <img src="https://images.mindcloud.co/apps/icons/tny_1775495011170.png" alt="Tny logo" width="28" height="28"> Tny: Universal API

API-first link shortener for creating short links, listing links, and retrieving link analytics.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tny/latest
- **Category:** Marketing
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.tny.dev
- **Vendor API docs:** https://www.tny.dev/api-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Links](actions/list-links.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tny/latest/actions/list-links?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Create Short Links](actions/bulk-create-short-links.md) | POST | Creates multiple shortened links in Tny. |
| [Create Short Link](actions/create-short-link.md) | POST | Creates a shortened link in Tny. |
| [Get Link Analytics](actions/get-link-analytics.md) | GET | Retrieves analytics for a short link from Tny. |
| [List Links](actions/list-links.md) | GET | Retrieves short links from Tny. |

