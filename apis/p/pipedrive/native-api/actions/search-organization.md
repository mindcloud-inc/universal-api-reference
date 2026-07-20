# Search Organizations with Pipedrive

Finds organizations in Pipedrive by search term.

## Endpoint

- **Method:** `GET`
- **Path:** `v2/organizations/search`
- **Base URL:** `{api_domain}/api`
- **Official documentation:** [Search Organizations](https://developers.pipedrive.com/docs/api/v1/Organizations#getOrganizationsSearch)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exact_match` | query | `string` | no | Set true to only return exact matches. |
| `fields` | query | `string` | no | Comma-separated fields to search in. |
| `term` | query | `string` | yes | Search term for organization name. |
| `limit` | query | `number` | no | Max number of records to return. |
| `cursor` | query | `string` | no | Pagination cursor from previous response. |
