# Find Similar Companies with Extruct AI

Finds similar companies in Extruct AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/companies/:company_identifier/similar`
- **Base URL:** `https://api.extruct.ai`
- **Official documentation:** [Find Similar Companies](https://docs.extruct.ai/api-reference/lookalike-search)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_identifier` | path | `string` | yes | Reference company UUID or domain. |
| `filters` | query | `string` | no | JSON string of SearchFilters. |
