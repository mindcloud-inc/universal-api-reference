# List Cash Movements with Hiboutik

Retrieves monthly cash movements for a store in Hiboutik.

## Endpoint

- **Method:** `GET`
- **Path:** `/till/:store_id/:year/:month`
- **Base URL:** `https://mindcloudhiboutik20260402.hiboutik.com/api`
- **Official documentation:** [List Cash Movements](https://mindcloudhiboutik20260402.hiboutik.com/docapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `month` | path | `string` | no | The numeric month. |
| `store_id` | path | `string` | no | The Hiboutik store id. |
| `year` | path | `string` | no | The four-digit year. |
