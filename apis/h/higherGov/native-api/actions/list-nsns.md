# List NSNs with HigherGov

Retrieves national stock numbers from HigherGov.

## Endpoint

- **Method:** `GET`
- **Path:** `/api-external/nsn/`
- **Base URL:** `https://www.highergov.com`
- **Official documentation:** [List NSNs](https://www.highergov.com/api-external/docs/#/api-external/api_external_nsn_list)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cage_code` | query | `string` | no | Supplier CAGE |
| `nsn` | query | `string` | no | National Stock Number |
| `part_number` | query | `string` | no | Part number |
