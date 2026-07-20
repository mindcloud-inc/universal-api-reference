# List Reporting Batch Items with Lasso X

Retrieves items for a reporting batch from Lasso X.

## Endpoint

- **Method:** `GET`
- **Path:** `/apps/reporting/batches/:id/items`
- **Base URL:** `https://api.lassox.com`
- **Official documentation:** [List Reporting Batch Items](https://docs.lassox.com/module-apis/reporting/#retrieve-reports)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Reporting batch ID. |
| `status` | query | `string` | no | Filter batch items by status, e.g. Completed. |
