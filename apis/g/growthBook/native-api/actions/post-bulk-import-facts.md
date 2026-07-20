# Bulk import fact tables, filters, and metrics with GrowthBook

Bulk imports fact tables, filters, and metrics into GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/bulk-import/facts`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Bulk import fact tables, filters, and metrics](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `factTables[]` | body | `array<object>` | no |
| `factTableFilters[]` | body | `array<object>` | no |
| `factMetrics[]` | body | `array<object>` | no |
