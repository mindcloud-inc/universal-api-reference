# Search Leads with Enrich.so

Finds leads in Enrich.so by search filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/lead-finder/search`
- **Base URL:** `https://dev.enrich.so/api/v3`
- **Official documentation:** [Search Leads](https://doc.enrich.so/search-leads-28165853e0.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | body | `object` | yes | Lead finder filter object. |
| `excludeFilters` | body | `object` | no | Optional filters to exclude. |
| `page` | body | `number` | no | Page number, starting at 1. |
| `pageSize` | body | `number` | no | Results per page. |
