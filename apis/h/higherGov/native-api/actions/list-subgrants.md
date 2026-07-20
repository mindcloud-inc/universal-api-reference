# List Subgrants with HigherGov

Retrieves subgrant awards from HigherGov.

## Endpoint

- **Method:** `GET`
- **Path:** `/api-external/subgrant/`
- **Base URL:** `https://www.highergov.com`
- **Official documentation:** [List Subgrants](https://www.highergov.com/api-external/docs/#/api-external/api_external_subgrant_list)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `awardee_key` | query | `string` | no | HigherGov Awardee Key |
| `awardee_uei` | query | `string` | no | Awardee UEI |
| `awarding_agency_key` | query | `string` | no | HigherGov Awarding Agency key |
| `funding_agency_key` | query | `string` | no | HigherGov Funding Agency key |
| `last_modified_date` | query | `string` | no | Last modified date filter in YYYY-MM-DD format |
