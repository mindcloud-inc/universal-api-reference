# <img src="https://images.mindcloud.co/apps/icons/search-apigoogle-search_1778080917977.png" alt="SearchAPI - Google Search logo" width="28" height="28"> SearchAPI - Google Search: Universal API

Search Google in real time through SearchAPI and retrieve structured search results, supported locations, and account usage data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/searchAPIGoogleSearch/latest
- **Category:** Marketing
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.searchapi.io/
- **Vendor API docs:** https://www.searchapi.io/docs/google

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Usage](actions/get-account-usage.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/searchAPIGoogleSearch/latest/actions/get-account-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Google Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Google](actions/search-google.md) | GET | Finds Google web search results in SearchAPI. |

### Searchapi Account Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Usage](actions/get-account-usage.md) | GET | Retrieves current account usage details from SearchAPI. |

### Supported Google Location

| Action | Method | Description |
| --- | --- | --- |
| [Find Supported Locations](actions/find-supported-locations.md) | GET | Finds supported Google search locations in SearchAPI. |

