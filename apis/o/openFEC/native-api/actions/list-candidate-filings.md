# List Candidate Filings with OpenFEC

Retrieves a candidate's filings from OpenFEC.

## Endpoint

- **Method:** `GET`
- **Path:** `/candidate/:candidate_id/filings/`
- **Base URL:** `https://api.open.fec.gov/v1`
- **Official documentation:** [List Candidate Filings](https://api.open.fec.gov/developers/)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `candidate_id` | path | `string` | yes | FEC candidate ID, such as P80000722. |
