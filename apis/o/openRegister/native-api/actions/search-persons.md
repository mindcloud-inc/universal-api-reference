# Search Persons with OpenRegister

Finds people in OpenRegister using advanced filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/search/person`
- **Base URL:** `https://api.openregister.de`
- **Official documentation:** [Search Persons](https://docs.openregister.de/endpoint/filter-person)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `object` | no | Person search query object. |
| `pagination` | body | `object` | no | Pagination parameters for person search. |
