# Search Companies with Extruct AI

Finds companies in Extruct AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/companies/search`
- **Base URL:** `https://api.extruct.ai`
- **Official documentation:** [Search Companies](https://docs.extruct.ai/api-reference/search)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Natural-language search query. |
| `filters` | query | `string` | no | JSON string of SearchFilters. |
