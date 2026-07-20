# Search with Freshsales Classic

Finds records in Freshsales Classic by query.

## Endpoint

- **Method:** `GET`
- **Path:** `/search`
- **Base URL:** `https://{bundleAlias}/api`
- **Official documentation:** [Search](https://developers.freshworks.com/crm/api/#search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include` | query | `string` | yes | Entity types to include in the search, for example contact, sales_account, deal, or user. |
| `page` | query | `number` | no | Page number to return. |
| `per_page` | query | `number` | no | Maximum number of results to return per page. |
| `q` | query | `string` | yes | Search text to look up in Freshsales Classic. |
