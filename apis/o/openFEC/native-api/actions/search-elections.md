# Search Elections with OpenFEC

Finds elections in OpenFEC by cycle, office, state, or district.

## Endpoint

- **Method:** `GET`
- **Path:** `/elections/search/`
- **Base URL:** `https://api.open.fec.gov/v1`
- **Official documentation:** [Search Elections](https://api.open.fec.gov/developers/)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cycle` | query | `number` | no | Two-year election cycle, such as 2024. |
| `office` | query | `string` | no | Federal office: president, senate, or house. Accepted values: `0`, `1`, `2`. |
