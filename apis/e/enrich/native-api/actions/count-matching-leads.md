# Count Matching Leads with Enrich.so

Retrieves lead counts from Enrich.so by search filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/lead-finder/count`
- **Base URL:** `https://dev.enrich.so/api/v3`
- **Official documentation:** [Count Matching Leads](https://doc.enrich.so/count-matching-leads-28165854e0.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | body | `object` | yes | Lead finder filter object. |
| `excludeFilters` | body | `object` | no | Optional filters to exclude. |
