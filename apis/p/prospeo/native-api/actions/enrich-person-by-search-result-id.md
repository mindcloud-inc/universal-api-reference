# Enrich Person by Search Result ID with Prospeo

Retrieves enriched person data from Prospeo by search result ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/enrich-person`
- **Base URL:** `https://api.prospeo.io`
- **Official documentation:** [Enrich Person by Search Result ID](https://prospeo.io/api-docs/enrich-person)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | Person identifier payload from a Prospeo search result. |
