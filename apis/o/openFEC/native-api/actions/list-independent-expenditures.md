# List Independent Expenditures with OpenFEC

Retrieves independent expenditures from OpenFEC.

## Endpoint

- **Method:** `GET`
- **Path:** `/schedules/schedule_e/`
- **Base URL:** `https://api.open.fec.gov/v1`
- **Official documentation:** [List Independent Expenditures](https://api.open.fec.gov/developers/)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `candidate_id` | query | `string` | no | Filter independent expenditures by FEC candidate ID. |
