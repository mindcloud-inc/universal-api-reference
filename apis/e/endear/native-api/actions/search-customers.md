# Search Customers with Endear

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.endearhq.com`
- **Official documentation:** [Search Customers](https://docs.endearhq.com/docs/graphql-pagination)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.first` | body | `number` | no | First for the Endear GraphQL operation. |
| `variables.after` | body | `string` | no | After for the Endear GraphQL operation. |
| `variables.sortBy` | body | `string` | no | Optional Endear customer sort field. |
| `variables.sortDir` | body | `string` | no | Optional Endear customer sort direction. |
| `variables.search` | body | `string` | no | Free-text search term for customers. |
| `variables.filters[]` | body | `array<object>` | no | Optional GraphQL SearchFilterInput array for customer filtering. |
