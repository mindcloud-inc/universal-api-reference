# List Committees with OpenFEC

Retrieves a list of committees from OpenFEC.

## Endpoint

- **Method:** `GET`
- **Path:** `/committees/`
- **Base URL:** `https://api.open.fec.gov/v1`
- **Official documentation:** [List Committees](https://api.open.fec.gov/developers/)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Committee name search text. |
