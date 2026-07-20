# List All Deals with Freshsales Classic

Retrieves deals from a Freshsales Classic view.

## Endpoint

- **Method:** `GET`
- **Path:** `/deals/view/:viewId`
- **Base URL:** `https://{bundleAlias}/api`
- **Official documentation:** [List All Deals](https://developers.freshworks.com/crm/api/#list_all_deals)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number to return for the selected deal view. |
| `viewId` | path | `number` | yes | The deal view ID. |
