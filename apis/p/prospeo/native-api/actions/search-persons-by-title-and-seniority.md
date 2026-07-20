# Search Persons by Title and Seniority with Prospeo

Finds persons in Prospeo by title and seniority.

## Endpoint

- **Method:** `POST`
- **Path:** `/search-person`
- **Base URL:** `https://api.prospeo.io`
- **Official documentation:** [Search Persons by Title and Seniority](https://prospeo.io/api-docs/search-person)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | body | `object` | yes | Person title and seniority search filters. |
