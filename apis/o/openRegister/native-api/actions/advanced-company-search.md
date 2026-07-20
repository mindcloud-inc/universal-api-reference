# Advanced Company Search with OpenRegister

Finds companies in OpenRegister using advanced filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/search/company`
- **Base URL:** `https://api.openregister.de`
- **Official documentation:** [Advanced Company Search](https://docs.openregister.de/endpoint/filter-company)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `object` | no | Advanced company search query object. |
| `filters[]` | body | `array<object>` | no | Advanced company search filters. Send multiple values as a array. |
| `pagination` | body | `object` | no | Pagination parameters for advanced company search. |
