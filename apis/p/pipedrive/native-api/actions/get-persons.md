# Get Persons with Pipedrive

Retrieves person records from Pipedrive.

## Endpoint

- **Method:** `GET`
- **Path:** `v2/persons`
- **Base URL:** `{api_domain}/api`
- **Official documentation:** [Get Persons](https://developers.pipedrive.com/docs/api/v1/Persons#getPersons)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of persons to return. |
| `cursor` | query | `string` | no | Pagination cursor from a previous response. |
| `sort_by` | query | `string` | no | Field used for sorting results. |
| `sort_direction` | query | `string` | no | Sort direction: asc or desc. |
| `owner_id` | query | `number` | no | Filter persons by owner user ID. |
| `filter_id` | query | `number` | no | Filter persons by saved filter ID. |
| `first_char` | query | `string` | no | Filter persons by the first character of name. |
| `ids` | query | `string` | no | Comma-separated list of person IDs. |
| `include_fields` | query | `string` | no | Comma-separated additional fields to include. |
| `custom_fields` | query | `string` | no | Comma-separated custom field keys to include. |
| `updated_since` | query | `string` | no | Return persons updated after this timestamp. |
