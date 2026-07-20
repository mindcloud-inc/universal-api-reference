# List Deals with Pipedrive

Retrieves deals from Pipedrive.

## Endpoint

- **Method:** `GET`
- **Path:** `v2/deals`
- **Base URL:** `{api_domain}/api`
- **Official documentation:** [List Deals](https://developers.pipedrive.com/docs/api/v1/Deals#getDealsCollection)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Filter by deal status: open, won, lost, deleted, or all_not_deleted. |
| `sort_by` | query | `string` | no | Sort field for returned deals. |
| `sort_direction` | query | `string` | no | Sort direction: asc or desc. |
| `updated_since` | query | `string` | no | Return deals updated after this timestamp. |
