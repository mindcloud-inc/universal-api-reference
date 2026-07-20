# List Disbursements with OpenFEC

Retrieves disbursements from OpenFEC.

## Endpoint

- **Method:** `GET`
- **Path:** `/schedules/schedule_b/`
- **Base URL:** `https://api.open.fec.gov/v1`
- **Official documentation:** [List Disbursements](https://api.open.fec.gov/developers/)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `committee_id` | query | `string` | no | Filter disbursements by FEC committee ID. |
