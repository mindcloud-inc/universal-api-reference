# Bulk Enrich Companies with People Data Labs

## Endpoint

- **Method:** `POST`
- **Path:** `/company/enrich/bulk`
- **Base URL:** `https://api.peopledatalabs.com/v5`
- **Official documentation:** [Bulk Enrich Companies](https://docs.peopledatalabs.com/docs/bulk-company-enrichment-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requests` | body | `list<object>` | yes | Array of 1-100 request objects, each containing a params object for one company enrichment call. |
