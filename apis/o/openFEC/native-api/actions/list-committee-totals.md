# List Committee Totals with OpenFEC

Retrieves committee financial totals from OpenFEC.

## Endpoint

- **Method:** `GET`
- **Path:** `/committee/:committee_id/totals/`
- **Base URL:** `https://api.open.fec.gov/v1`
- **Official documentation:** [List Committee Totals](https://api.open.fec.gov/developers/)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `committee_id` | path | `string` | yes | FEC committee ID, such as C00580100. |
