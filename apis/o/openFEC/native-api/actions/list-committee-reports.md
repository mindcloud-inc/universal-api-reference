# List Committee Reports with OpenFEC

Retrieves committee reports from OpenFEC.

## Endpoint

- **Method:** `GET`
- **Path:** `/committee/:committee_id/reports/`
- **Base URL:** `https://api.open.fec.gov/v1`
- **Official documentation:** [List Committee Reports](https://api.open.fec.gov/developers/)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `committee_id` | path | `string` | yes | FEC committee ID, such as C00580100. |
| `cycle` | query | `number` | no | Two-year election cycle, such as 2024. |
