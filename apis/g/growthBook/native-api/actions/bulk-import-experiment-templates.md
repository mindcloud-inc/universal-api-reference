# Bulk create or update experiment templates with GrowthBook

Bulk creates or updates experiment templates in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/experiment-templates/bulk-import`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Bulk create or update experiment templates](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `templates[]` | body | `array<object>` | yes |
