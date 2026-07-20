# List IDV Awards with HigherGov

Retrieves federal IDV awards from HigherGov.

## Endpoint

- **Method:** `GET`
- **Path:** `/api-external/idv/`
- **Base URL:** `https://www.highergov.com`
- **Official documentation:** [List IDV Awards](https://www.highergov.com/api-external/docs/#/api-external/api_external_idv_list)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `award_id` | query | `string` | no | Government Award ID |
| `awardee_key` | query | `string` | no | HigherGov Awardee Key |
| `awardee_uei` | query | `string` | no | Awardee UEI |
| `awarding_agency_key` | query | `string` | no | HigherGov Awarding Agency key |
| `funding_agency_key` | query | `string` | no | HigherGov Funding Agency key |
| `last_modified_date` | query | `string` | no | Last modified date filter in YYYY-MM-DD format |
| `naics_code` | query | `string` | no | Award NAICS code |
| `psc_code` | query | `string` | no | Product Service Code |
| `vehicle_key` | query | `string` | no | HigherGov Vehicle key |
