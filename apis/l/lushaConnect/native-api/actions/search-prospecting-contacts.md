# Search Prospecting Contacts with Lusha Connect

Finds prospecting contacts in Lusha Connect by filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/prospecting/contact/search`
- **Base URL:** `https://api.lusha.com`
- **Official documentation:** [Search Prospecting Contacts](https://docs.lusha.com/apis/openapi/prospecting-search-and-enrich/searchprospectingcontacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pages` | body | `object` | no | Pagination settings for the prospecting contact search. Lusha requires size to be at least 10. |
| `filters` | body | `object` | yes | Prospecting contact and company filters object following the official Lusha schema. |
