# Search Drugs with Cerbo

Finds drugs in Cerbo by search term.

## Endpoint

- **Method:** `GET`
- **Path:** `/drugs/search/:term`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Search Drugs](https://docs.cer.bo/#tag/Drugs/operation/searchDrugs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `term` | path | `string` | yes | Search term for drug name |
| `favorites-only` | query | `boolean` | no | Return only drugs from provider's favorites list |
