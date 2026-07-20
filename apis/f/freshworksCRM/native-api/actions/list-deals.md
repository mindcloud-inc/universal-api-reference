# List Deals with Freshworks CRM

Retrieves deals from a view in Freshworks CRM.

## Endpoint

- **Method:** `GET`
- **Path:** `api/deals/view/:view_id`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [List Deals](https://developers.freshworks.com/crm/api/#list_all_deals)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `view_id` | path | `number` | no | Numeric view identifier used for list queries. |
