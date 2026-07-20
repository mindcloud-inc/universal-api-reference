# List All Accounts with Freshsales Classic

Retrieves accounts from a Freshsales Classic view.

## Endpoint

- **Method:** `GET`
- **Path:** `/sales_accounts/view/:viewId`
- **Base URL:** `https://{bundleAlias}/api`
- **Official documentation:** [List All Accounts](https://developers.freshworks.com/crm/api/#list_all_accounts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number to return for the selected account view. |
| `viewId` | path | `number` | yes | The account view ID. |
