# <img src="https://images.mindcloud.co/apps/icons/e-cfr_1777482228667.png" alt="eCFR logo" width="28" height="28"> eCFR: Universal API

Access the Electronic Code of Federal Regulations, including title metadata, agency metadata, search results, corrections, version history, structure, ancestry, and full title content from the public eCFR API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eCFR/latest
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ecfr.gov
- **Vendor API docs:** https://www.ecfr.gov/developers/documentation/api/v1

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Titles](actions/list-titles.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/list-titles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Agency

| Action | Method | Description |
| --- | --- | --- |
| [List Agencies](actions/list-agencies.md) | GET | Retrieves a list of agencies from eCFR. |

### Cfr Ancestry

| Action | Method | Description |
| --- | --- | --- |
| [Get Title Ancestry](actions/get-title-ancestry.md) | GET | Retrieves the ancestry for a title from eCFR. |

### Cfr Structure

| Action | Method | Description |
| --- | --- | --- |
| [Get Title Structure](actions/get-title-structure.md) | GET | Retrieves a title structure from eCFR. |

### Cfr Title

| Action | Method | Description |
| --- | --- | --- |
| [List Titles](actions/list-titles.md) | GET | Retrieves a list of titles from eCFR. |

### Cfr Version

| Action | Method | Description |
| --- | --- | --- |
| [List Title Versions](actions/list-title-versions.md) | GET | Retrieves the available versions for a title from eCFR. |

### Cfr Xml Content

| Action | Method | Description |
| --- | --- | --- |
| [Get Full Title XML](actions/get-full-title-xml.md) | GET | Retrieves the full XML for a title from eCFR. |

### Correction

| Action | Method | Description |
| --- | --- | --- |
| [List Corrections](actions/list-corrections.md) | GET | Retrieves a list of corrections from eCFR. |

### Daily Search Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Daily Search Counts](actions/get-daily-search-counts.md) | GET | Retrieves daily search result counts from eCFR. |

### Hierarchy Search Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Hierarchy Search Counts](actions/get-hierarchy-search-counts.md) | GET | Retrieves search result counts by hierarchy from eCFR. |

### Imported Cfr Title

| Action | Method | Description |
| --- | --- | --- |
| [List Imported Titles](actions/list-imported-titles.md) | GET | Retrieves a list of imported titles from eCFR. |

### Search Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Search Results](actions/count-search-results.md) | GET | Retrieves the count of search results from eCFR. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Regulations](actions/search-regulations.md) | GET | Searches regulations in eCFR by keyword. |

### Search Suggestion

| Action | Method | Description |
| --- | --- | --- |
| [Get Search Suggestions](actions/get-search-suggestions.md) | GET | Retrieves search suggestions for a query from eCFR. |

### Search Summary

| Action | Method | Description |
| --- | --- | --- |
| [Summarize Search Results](actions/summarize-search-results.md) | GET | Retrieves summary details for search results from eCFR. |

### Title Search Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Title Search Counts](actions/get-title-search-counts.md) | GET | Retrieves search result counts by title from eCFR. |

