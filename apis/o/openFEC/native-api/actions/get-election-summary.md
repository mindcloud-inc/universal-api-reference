# Get Election Summary with OpenFEC

Retrieves an election summary from OpenFEC.

## Endpoint

- **Method:** `GET`
- **Path:** `/elections/summary/`
- **Base URL:** `https://api.open.fec.gov/v1`
- **Official documentation:** [Get Election Summary](https://api.open.fec.gov/developers/)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cycle` | query | `number` | yes | Two-year election cycle, such as 2024. |
| `office` | query | `string` | yes | Federal office: president, senate, or house. Accepted values: `0`, `1`, `2`. |
