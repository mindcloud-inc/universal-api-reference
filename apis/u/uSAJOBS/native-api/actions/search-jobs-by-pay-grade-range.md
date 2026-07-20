# Search Jobs By Pay Grade Range with USAJOBS

Finds jobs in USAJOBS by pay grade range.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/Search`
- **Base URL:** `https://data.usajobs.gov`
- **Official documentation:** [Search Jobs By Pay Grade Range](https://developer.usajobs.gov/api-reference/get-api-search)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PayGradeHigh` | query | `string` | no | Maximum GS-equivalent grade from 01 through 15. |
| `PayGradeLow` | query | `string` | no | Minimum GS-equivalent grade from 01 through 15. |
