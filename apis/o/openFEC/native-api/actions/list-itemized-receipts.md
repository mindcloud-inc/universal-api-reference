# List Itemized Receipts with OpenFEC

Retrieves itemized receipts from OpenFEC.

## Endpoint

- **Method:** `GET`
- **Path:** `/schedules/schedule_a/`
- **Base URL:** `https://api.open.fec.gov/v1`
- **Official documentation:** [List Itemized Receipts](https://api.open.fec.gov/developers/)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `committee_id` | query | `string` | no | Filter receipts by FEC committee ID. |
