# List Products Purchased with Hiboutik

Retrieves purchased products for a specific date in Hiboutik.

## Endpoint

- **Method:** `GET`
- **Path:** `/products_purchased/:warehouse_id/:year/:month/:day/`
- **Base URL:** `https://mindcloudhiboutik20260402.hiboutik.com/api`
- **Official documentation:** [List Products Purchased](https://mindcloudhiboutik20260402.hiboutik.com/docapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `day` | path | `string` | no | The numeric day. |
| `month` | path | `string` | no | The numeric month. |
| `warehouse_id` | path | `string` | no | The Hiboutik warehouse id. |
| `year` | path | `string` | no | The four-digit year. |
