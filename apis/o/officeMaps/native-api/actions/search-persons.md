# Search Persons with OfficeMaps

Finds people in OfficeMaps by search filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/person`
- **Base URL:** `https://api.officemaps.io`
- **Official documentation:** [Search Persons](https://api.officemaps.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `SearchTerm` | query | `string` | no | Filter persons by a general search term. |
| `Sort` | query | `string` | no | Sort expression for the search results. |
| `PageSize` | query | `number` | no | Maximum number of persons per page. |
| `Page` | query | `number` | no | Page number for the search results. |
