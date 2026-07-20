# Enrich Person with Mobile with Prospeo

Retrieves enriched person data from Prospeo with mobile numbers.

## Endpoint

- **Method:** `POST`
- **Path:** `/enrich-person`
- **Base URL:** `https://api.prospeo.io`
- **Official documentation:** [Enrich Person with Mobile](https://prospeo.io/api-docs/enrich-person)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | Person datapoints used for matching. |
