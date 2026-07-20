# Search Persons by Company List with Prospeo

Finds persons in Prospeo by company list.

## Endpoint

- **Method:** `POST`
- **Path:** `/search-person`
- **Base URL:** `https://api.prospeo.io`
- **Official documentation:** [Search Persons by Company List](https://prospeo.io/api-docs/search-person)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | body | `object` | yes | Person search filters using company websites or names. |
