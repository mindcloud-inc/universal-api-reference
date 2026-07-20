# Get Accounting Invoice with Merge

## Endpoint

- **Method:** `GET`
- **Path:** `/api/accounting/v1/invoices/{id}`
- **Base URL:** `https://api.merge.dev`
- **Official documentation:** [Get Accounting Invoice](https://docs.merge.dev/accounting/invoices/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountToken` | query | `string` | yes | Linked account token for the Merge account you want to query. The shared headers mapper sends this input as X-Account-Token. |
| `id` | path | `string` | yes | Merge object ID. |
