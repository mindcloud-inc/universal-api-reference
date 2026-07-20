# Enrich Person with Prospeo

Retrieves enriched person data from Prospeo.

## Endpoint

- **Method:** `POST`
- **Path:** `/enrich-person`
- **Base URL:** `https://api.prospeo.io`
- **Official documentation:** [Enrich Person](https://prospeo.io/api-docs/enrich-person)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | Person datapoints used for matching. |
