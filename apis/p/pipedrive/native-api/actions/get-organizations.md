# Get Organizations with Pipedrive

Retrieves organizations from Pipedrive.

## Endpoint

- **Method:** `GET`
- **Path:** `v2/organizations`
- **Base URL:** `{api_domain}/api`
- **Official documentation:** [Get Organizations](https://developers.pipedrive.com/docs/api/v1/Organizations#getOrganizations)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of organizations to return. |
| `cursor` | query | `string` | no | Pagination cursor from a previous response. |
| `sort_by` | query | `string` | no | Field used for sorting results. |
| `sort_direction` | query | `string` | no | Sort direction: asc or desc. |
| `owner_id` | query | `number` | no | Filter organizations by owner user ID. |
| `filter_id` | query | `number` | no | Filter organizations by saved filter ID. |
| `first_char` | query | `string` | no | Filter organizations by first character of name. |
| `ids` | query | `string` | no | Comma-separated list of organization IDs. |
| `include_fields` | query | `string` | no | Comma-separated additional fields to include. |
| `custom_fields` | query | `string` | no | Comma-separated custom field keys to include. |
| `updated_since` | query | `string` | no | Return organizations updated after this timestamp. |
