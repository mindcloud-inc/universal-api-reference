# <img src="https://images.mindcloud.co/apps/icons/google-search-console-icon-vector-brandlogos_1784123785337.png" alt="Google Search Console logo" width="28" height="28"> Google Search Console: Universal API

Monitor search performance, manage properties and sitemaps, and inspect URLs

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/googleSearchConsole/latest
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://search.google.com/search-console/about
- **Vendor API docs:** https://developers.google.com/webmaster-tools/v1/api_reference_index

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Sites](actions/list-sites.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleSearchConsole/latest/actions/list-sites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Search Analytics Row

| Action | Method | Description |
| --- | --- | --- |
| [Query Search Analytics](actions/query-search-analytics.md) | GET |  |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [Add Site](actions/add-site.md) | POST |  |
| [Delete Site](actions/delete-site.md) | DELETE |  |
| [Get Site](actions/get-site.md) | GET |  |
| [List Sites](actions/list-sites.md) | GET |  |

### Sitemap

| Action | Method | Description |
| --- | --- | --- |
| [Delete Sitemap](actions/delete-sitemap.md) | DELETE |  |
| [Get Sitemap](actions/get-sitemap.md) | GET |  |
| [List Sitemaps](actions/list-sitemaps.md) | GET |  |
| [Submit Sitemap](actions/submit-sitemap.md) | POST |  |

### Url Inspector

| Action | Method | Description |
| --- | --- | --- |
| [Inspect URL](actions/inspect-url.md) | GET |  |

