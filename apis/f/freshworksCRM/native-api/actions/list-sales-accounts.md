# List Sales Accounts with Freshworks CRM

Retrieves sales accounts from a view in Freshworks CRM.

## Endpoint

- **Method:** `GET`
- **Path:** `api/sales_accounts/view/:view_id`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [List Sales Accounts](https://developers.freshworks.com/crm/api/#list_all_accounts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `view_id` | path | `number` | no | Numeric view identifier used for list queries. |
