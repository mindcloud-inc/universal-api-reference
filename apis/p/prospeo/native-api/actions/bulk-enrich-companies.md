# Bulk Enrich Companies with Prospeo

Retrieves enriched company data from Prospeo in bulk.

## Endpoint

- **Method:** `POST`
- **Path:** `/bulk-enrich-company`
- **Base URL:** `https://api.prospeo.io`
- **Official documentation:** [Bulk Enrich Companies](https://prospeo.io/api-docs/bulk-enrich-company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array<object>` | yes | Company records to enrich, up to 50 at once. |
