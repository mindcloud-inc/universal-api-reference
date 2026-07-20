# Search Legal Documents with OpenFEC

Finds legal documents in OpenFEC by search terms.

## Endpoint

- **Method:** `GET`
- **Path:** `/legal/search/`
- **Base URL:** `https://api.open.fec.gov/v1`
- **Official documentation:** [Search Legal Documents](https://api.open.fec.gov/developers/)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Word or phrase to search across legal documents. |
