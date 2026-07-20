# Search Candidates with OpenFEC

Finds candidates in OpenFEC by search terms.

## Endpoint

- **Method:** `GET`
- **Path:** `/candidates/search/`
- **Base URL:** `https://api.open.fec.gov/v1`
- **Official documentation:** [Search Candidates](https://api.open.fec.gov/developers/)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Candidate name search text. |
