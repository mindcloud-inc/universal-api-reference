# List Committee History with OpenFEC

Retrieves a committee's history from OpenFEC.

## Endpoint

- **Method:** `GET`
- **Path:** `/committee/:committee_id/history/`
- **Base URL:** `https://api.open.fec.gov/v1`
- **Official documentation:** [List Committee History](https://api.open.fec.gov/developers/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `committee_id` | path | `string` | yes | FEC committee ID, such as C00580100. |
