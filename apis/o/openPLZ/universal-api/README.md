# <img src="https://images.mindcloud.co/apps/icons/open-plz_1777566296892.png" alt="OpenPLZ logo" width="28" height="28"> OpenPLZ: Universal API

Public street, postal code, locality, and administrative directory API for Austria, Germany, Liechtenstein, and Switzerland.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/openPLZ/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.openplzapi.org
- **Vendor API docs:** https://www.openplzapi.org/en/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Full Text Search Austria](actions/full-text-search-austria.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openPLZ/latest/actions/full-text-search-austria?connectionId=$CONNECTION_ID&limit=25&offset=0&searchTerm=Wien%20Stephansplatz" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Austrian Address Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Full Text Search Austria](actions/full-text-search-austria.md) | GET |  |

### Austrian District

| Action | Method | Description |
| --- | --- | --- |
| [List Austrian Districts by Federal Province](actions/list-austrian-districts-by-federal-province.md) | GET |  |

### Austrian Federal Province

| Action | Method | Description |
| --- | --- | --- |
| [List Austrian Federal Provinces](actions/list-austrian-federal-provinces.md) | GET |  |

### Austrian Locality

| Action | Method | Description |
| --- | --- | --- |
| [Search Austrian Localities](actions/search-austrian-localities.md) | GET |  |

### Austrian Municipality

| Action | Method | Description |
| --- | --- | --- |
| [List Austrian Municipalities by Federal Province](actions/list-austrian-municipalities-by-federal-province.md) | GET |  |

### Austrian Street

| Action | Method | Description |
| --- | --- | --- |
| [Search Austrian Streets](actions/search-austrian-streets.md) | GET |  |

### German Address Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Full Text Search Germany](actions/full-text-search-germany.md) | GET |  |

### German District

| Action | Method | Description |
| --- | --- | --- |
| [List German Districts by Federal State](actions/list-german-districts-by-federal-state.md) | GET |  |

### German Federal State

| Action | Method | Description |
| --- | --- | --- |
| [List German Federal States](actions/list-german-federal-states.md) | GET |  |

### German Government Region

| Action | Method | Description |
| --- | --- | --- |
| [List German Government Regions by Federal State](actions/list-german-government-regions-by-federal-state.md) | GET |  |

### German Locality

| Action | Method | Description |
| --- | --- | --- |
| [Search German Localities](actions/search-german-localities.md) | GET |  |

### German Municipality

| Action | Method | Description |
| --- | --- | --- |
| [List German Municipalities by Federal State](actions/list-german-municipalities-by-federal-state.md) | GET |  |

### German Street

| Action | Method | Description |
| --- | --- | --- |
| [Search German Streets](actions/search-german-streets.md) | GET |  |

### Liechtenstein Address Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Full Text Search Liechtenstein](actions/full-text-search-liechtenstein.md) | GET |  |

### Liechtenstein Commune

| Action | Method | Description |
| --- | --- | --- |
| [List Liechtenstein Communes](actions/list-liechtenstein-communes.md) | GET |  |

### Liechtenstein Locality

| Action | Method | Description |
| --- | --- | --- |
| [Search Liechtenstein Localities](actions/search-liechtenstein-localities.md) | GET |  |

### Liechtenstein Street

| Action | Method | Description |
| --- | --- | --- |
| [Search Liechtenstein Streets](actions/search-liechtenstein-streets.md) | GET |  |

### Swiss Address Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Full Text Search Switzerland](actions/full-text-search-switzerland.md) | GET |  |

### Swiss Canton

| Action | Method | Description |
| --- | --- | --- |
| [List Swiss Cantons](actions/list-swiss-cantons.md) | GET |  |

### Swiss Commune

| Action | Method | Description |
| --- | --- | --- |
| [List Swiss Communes by Canton](actions/list-swiss-communes-by-canton.md) | GET |  |

### Swiss District

| Action | Method | Description |
| --- | --- | --- |
| [List Swiss Districts by Canton](actions/list-swiss-districts-by-canton.md) | GET |  |

### Swiss Locality

| Action | Method | Description |
| --- | --- | --- |
| [List Swiss Localities by Canton](actions/list-swiss-localities-by-canton.md) | GET |  |
| [Search Swiss Localities](actions/search-swiss-localities.md) | GET |  |

### Swiss Street

| Action | Method | Description |
| --- | --- | --- |
| [Search Swiss Streets](actions/search-swiss-streets.md) | GET |  |

