# Search Persons with Verified Contact Details with Prospeo

Finds persons in Prospeo with verified contact details.

## Endpoint

- **Method:** `POST`
- **Path:** `/search-person`
- **Base URL:** `https://api.prospeo.io`
- **Official documentation:** [Search Persons with Verified Contact Details](https://prospeo.io/api-docs/search-person)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | body | `object` | yes | Person search filters likely to return verified contact details for enrichment. |
