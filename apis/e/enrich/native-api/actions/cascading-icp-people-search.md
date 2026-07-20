# Cascading ICP People Search with Enrich.so

Finds people in Enrich.so by cascading ICP filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/people-search/waterfall-icp-search`
- **Base URL:** `https://dev.enrich.so/api/v3`
- **Official documentation:** [Cascading ICP People Search](https://doc.enrich.so/cascading-icp-people-search-28537859e0.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_linkedin_url` | body | `string` | yes | LinkedIn company URL to search. |
| `cascade[]` | body | `array<object>` | no | Optional cascade filter levels. |
