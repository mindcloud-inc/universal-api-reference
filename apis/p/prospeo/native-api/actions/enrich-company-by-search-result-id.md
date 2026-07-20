# Enrich Company by Search Result ID with Prospeo

Retrieves enriched company data from Prospeo by search result ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/enrich-company`
- **Base URL:** `https://api.prospeo.io`
- **Official documentation:** [Enrich Company by Search Result ID](https://prospeo.io/api-docs/enrich-company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | Company identifier payload from a Prospeo search or enriched company object. |
