# <img src="https://images.mindcloud.co/apps/icons/automn-light_1775489473749.png" alt="Autom logo" width="28" height="28"> Autom: Universal API

Developer-first scraping API for Google, Brave, Bing, and related search engines.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/autom/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.autom.dev
- **Vendor API docs:** https://docs.autom.dev/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Usage](actions/get-usage.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/autom/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [Search Bing](actions/search-bing.md) | GET | Finds Bing search results in Autom. |
| [Search Brave](actions/search-brave.md) | GET | Finds Brave search results in Autom. |
| [Search Google](actions/search-google.md) | GET | Finds Google search results in Autom. |
| [Search Google Autocomplete Suggestions](actions/search-google-autocomplete-suggestions.md) | GET | Finds Google autocomplete suggestions in Autom. |
| [Search Google Images](actions/search-google-images.md) | GET | Finds Google image results in Autom. |
| [Search Google News](actions/search-google-news.md) | GET | Finds Google news results in Autom. |
| [Search Google Videos](actions/search-google-videos.md) | GET | Finds Google video results in Autom. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Usage](actions/get-usage.md) | GET | Retrieves usage details from Autom. |

