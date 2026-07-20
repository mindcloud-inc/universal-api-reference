# Enrich Company with Prospeo

Retrieves enriched company data from Prospeo.

## Endpoint

- **Method:** `POST`
- **Path:** `/enrich-company`
- **Base URL:** `https://api.prospeo.io`
- **Official documentation:** [Enrich Company](https://prospeo.io/api-docs/enrich-company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | Company datapoints used for matching. |
