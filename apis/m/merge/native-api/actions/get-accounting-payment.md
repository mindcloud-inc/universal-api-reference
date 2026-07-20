# Get Accounting Payment with Merge

## Endpoint

- **Method:** `GET`
- **Path:** `/api/accounting/v1/payments/{id}`
- **Base URL:** `https://api.merge.dev`
- **Official documentation:** [Get Accounting Payment](https://docs.merge.dev/accounting/payments/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountToken` | query | `string` | yes | Linked account token for the Merge account you want to query. The shared headers mapper sends this input as X-Account-Token. |
| `id` | path | `string` | yes | Merge object ID. |
