# Search Deals with Pipedrive

Finds deals in Pipedrive by search term.

## Endpoint

- **Method:** `GET`
- **Path:** `v2/deals/search`
- **Base URL:** `{api_domain}/api`
- **Official documentation:** [Search Deals](https://developers.pipedrive.com/docs/api/v1/Deals#searchDeals)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor` | query | `string` | no | Pagination cursor. |
| `fields` | query | `string` | no | Fields to search in. |
| `include_fields` | query | `string` | no | Comma-separated additional fields to include. |
| `status` | query | `string` | no | Filter by deal status. |
| `term` | query | `string` | yes | Search term for deals. |
| `exact_match` | query | `boolean` | no | Match term exactly. |
| `person_id` | query | `number` | no | Filter by person ID. |
| `organization_id` | query | `number` | no | Filter by organization ID. |
| `limit` | query | `number` | no | Max results per page. |
