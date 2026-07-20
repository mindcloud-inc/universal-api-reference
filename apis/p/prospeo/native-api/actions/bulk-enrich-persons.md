# Bulk Enrich Persons with Prospeo

Retrieves enriched person data from Prospeo in bulk.

## Endpoint

- **Method:** `POST`
- **Path:** `/bulk-enrich-person`
- **Base URL:** `https://api.prospeo.io`
- **Official documentation:** [Bulk Enrich Persons](https://prospeo.io/api-docs/bulk-enrich-person)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array<object>` | yes | Person records to enrich, up to 50 at once. |
| `only_verified_email` | body | `boolean` | no | Only return records with a verified email. |
| `enrich_mobile` | body | `boolean` | no | Enrich mobile phone data when available. |
