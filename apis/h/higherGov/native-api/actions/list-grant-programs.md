# List Grant Programs with HigherGov

Retrieves grant programs from HigherGov.

## Endpoint

- **Method:** `GET`
- **Path:** `/api-external/grant-program/`
- **Base URL:** `https://www.highergov.com`
- **Official documentation:** [List Grant Programs](https://www.highergov.com/api-external/docs/#/api-external/api_external_grant_program_list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agency_key` | query | `string` | no | HigherGov Agency key |
| `cfda_program_number` | query | `string` | no | CFDA program number for the grant program |
