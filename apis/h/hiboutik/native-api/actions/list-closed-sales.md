# List Closed Sales with Hiboutik

Retrieves closed sales for a specific date in Hiboutik.

## Endpoint

- **Method:** `GET`
- **Path:** `/closed_sales/:store_id/:year/:month/:day`
- **Base URL:** `https://mindcloudhiboutik20260402.hiboutik.com/api`
- **Official documentation:** [List Closed Sales](https://mindcloudhiboutik20260402.hiboutik.com/docapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `day` | path | `string` | no | The numeric day. |
| `month` | path | `string` | no | The numeric month. |
| `store_id` | path | `string` | no | The Hiboutik store id. |
| `year` | path | `string` | no | The four-digit year. |
