# List Opportunities with HigherGov

Retrieves government opportunities from HigherGov.

## Endpoint

- **Method:** `GET`
- **Path:** `/api-external/opportunity/`
- **Base URL:** `https://www.highergov.com`
- **Official documentation:** [List Opportunities](https://www.highergov.com/api-external/docs/#/api-external/api_external_opportunity_list)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agency_key` | query | `string` | no | HigherGov Agency key |
| `captured_date` | query | `string` | no | Date the opportunity was added to HigherGov |
| `opp_key` | query | `string` | no | HigherGov opportunity key |
| `posted_date` | query | `string` | no | Date the opportunity was posted in YYYY-MM-DD format |
| `search_id` | query | `string` | no | HigherGov SearchID |
| `source_id` | query | `string` | no | Source opportunity ID |
| `source_type` | query | `string` | no | Opportunity source type (sam, dibbs, sbir, grant, sled) |
| `version_key` | query | `string` | no | HigherGov opportunity version key |
