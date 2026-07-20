# Suggest Company Names with Enrich.so

Finds company name suggestions in Enrich.so.

## Endpoint

- **Method:** `GET`
- **Path:** `/lead-finder/suggest`
- **Base URL:** `https://dev.enrich.so/api/v3`
- **Official documentation:** [Suggest Company Names](https://doc.enrich.so/suggest-company-names-28165863e0.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Company name prefix to suggest. |
