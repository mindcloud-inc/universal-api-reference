# Search Persons with Pipedrive

Finds people in Pipedrive by search term.

## Endpoint

- **Method:** `GET`
- **Path:** `v2/persons/search`
- **Base URL:** `{api_domain}/api`
- **Official documentation:** [Search Persons](https://developers.pipedrive.com/docs/api/v1/Persons#searchPersons)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `term` | query | `string` | yes | Search term for persons. |
| `fields` | query | `string` | no | Comma-separated fields to search in. |
| `exact_match` | query | `boolean` | no | Set true to return only exact matches. |
| `organization_id` | query | `number` | no | Limit search to a specific organization ID. |
| `person_id` | query | `number` | no | Limit search to a specific person ID. |
| `include_fields` | query | `string` | no | Comma-separated additional fields to include. |
| `custom_fields` | query | `string` | no | Comma-separated custom field keys to include. |
| `limit` | query | `number` | no | Maximum number of search results to return. |
| `cursor` | query | `string` | no | Pagination cursor from previous search results. |
