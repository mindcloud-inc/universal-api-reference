# List Categories with G2

Retrieves categories from G2.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/categories`
- **Base URL:** `https://data.g2.com`
- **Official documentation:** [List Categories](https://data.g2.com/openapi/v2.yaml)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `fields[categories][]` | query | `array<string>` | no |
| `filter[created_at_gt]` | query | `date` | no |
| `filter[created_at_lt]` | query | `date` | no |
| `filter[name_cont]` | query | `string` | no |
| `filter[name_eq]` | query | `string` | no |
| `filter[slug_cont]` | query | `string` | no |
| `filter[slug_eq]` | query | `string` | no |
| `filter[updated_at_gt]` | query | `date` | no |
| `filter[updated_at_lt]` | query | `date` | no |
| `include[]` | query | `array<string>` | no |
