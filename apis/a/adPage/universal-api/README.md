# <img src="https://images.mindcloud.co/apps/icons/64e872fc32280818ec06932a-ad-page-favicon-1-svg_1774963440652.png" alt="AdPage logo" width="28" height="28"> AdPage: Universal API

Create landing pages, popups, and route leads with AdPage

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/adPage/latest
- **Category:** Marketing
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.adpage.io/
- **Vendor API docs:** https://whitelabel.adpage.io/api/doc

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Agency](actions/get-agency.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adPage/latest/actions/get-agency?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Agency

| Action | Method | Description |
| --- | --- | --- |
| [Get Agency](actions/get-agency.md) | GET | Retrieves the current agency from AdPage. |
| [Search Agencies](actions/search-agencies.md) | GET | Finds agencies in AdPage by name. |

### Section Category Catalog

| Action | Method | Description |
| --- | --- | --- |
| [List Section Categories](actions/list-section-categories.md) | GET | Retrieves section categories from AdPage. |

