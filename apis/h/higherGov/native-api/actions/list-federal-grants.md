# List Federal Grants with HigherGov

Retrieves federal grant awards from HigherGov.

## Endpoint

- **Method:** `GET`
- **Path:** `/api-external/grant/`
- **Base URL:** `https://www.highergov.com`
- **Official documentation:** [List Federal Grants](https://www.highergov.com/api-external/docs/#/api-external/api_external_grant_list)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `award_id` | query | `string` | no | Government Award ID |
| `awardee_key` | query | `string` | no | HigherGov Awardee Key |
| `awardee_uei` | query | `string` | no | Awardee UEI |
| `awarding_agency_key` | query | `string` | no | HigherGov Awarding Agency key |
| `cfda_program_number` | query | `string` | no | Grant Program Number (CFDA) |
| `funding_agency_key` | query | `string` | no | HigherGov Funding Agency key |
| `last_modified_date` | query | `string` | no | Last modified date filter in YYYY-MM-DD format |
| `search_id` | query | `string` | no | HigherGov SearchID |
