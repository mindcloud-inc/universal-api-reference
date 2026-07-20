# List Reports By Entity Type with OpenFEC

Retrieves reports in OpenFEC by entity type.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/:entity_type/`
- **Base URL:** `https://api.open.fec.gov/v1`
- **Official documentation:** [List Reports By Entity Type](https://api.open.fec.gov/developers/)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity_type` | path | `string` | yes | Committee grouping, such as presidential, senate, house-senate, pac-party, or ie-only. |
