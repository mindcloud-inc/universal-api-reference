# List NAICS Codes with HigherGov

Retrieves NAICS codes from HigherGov.

## Endpoint

- **Method:** `GET`
- **Path:** `/api-external/naics/`
- **Base URL:** `https://www.highergov.com`
- **Official documentation:** [List NAICS Codes](https://www.highergov.com/api-external/docs/#/api-external/api_external_naics_list)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `naics_code` | query | `string` | no | Awards NAICS code |
