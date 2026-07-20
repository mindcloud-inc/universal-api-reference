# List Candidates with OpenFEC

Retrieves a list of candidates from OpenFEC.

## Endpoint

- **Method:** `GET`
- **Path:** `/candidates/`
- **Base URL:** `https://api.open.fec.gov/v1`
- **Official documentation:** [List Candidates](https://api.open.fec.gov/developers/)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Candidate name search text. |
