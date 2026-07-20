# Search Jobs By Work Type with USAJOBS

Finds jobs in USAJOBS by work type.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/Search`
- **Base URL:** `https://data.usajobs.gov`
- **Official documentation:** [Search Jobs By Work Type](https://developer.usajobs.gov/api-reference/get-api-search)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PositionOfferingTypeCode` | query | `string` | no | Position offering/work type code. |
