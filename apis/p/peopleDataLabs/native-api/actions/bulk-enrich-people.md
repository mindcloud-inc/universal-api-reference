# Bulk Enrich People with People Data Labs

## Endpoint

- **Method:** `POST`
- **Path:** `/person/bulk`
- **Base URL:** `https://api.peopledatalabs.com/v5`
- **Official documentation:** [Bulk Enrich People](https://docs.peopledatalabs.com/docs/bulk-enrichment-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requests` | body | `list<object>` | yes | Array of 1-100 request objects, each containing a params object for one person enrichment call. |
