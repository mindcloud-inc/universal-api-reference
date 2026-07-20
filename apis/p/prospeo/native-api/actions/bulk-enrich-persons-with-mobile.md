# Bulk Enrich Persons with Mobile with Prospeo

Retrieves enriched person data from Prospeo in bulk with mobile numbers.

## Endpoint

- **Method:** `POST`
- **Path:** `/bulk-enrich-person`
- **Base URL:** `https://api.prospeo.io`
- **Official documentation:** [Bulk Enrich Persons with Mobile](https://prospeo.io/api-docs/bulk-enrich-person)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array<object>` | yes | Person records to enrich, up to 50 at once. |
