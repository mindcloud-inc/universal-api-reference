# List Accounting Invoices with Merge

## Endpoint

- **Method:** `GET`
- **Path:** `/api/accounting/v1/invoices`
- **Base URL:** `https://api.merge.dev`
- **Official documentation:** [List Accounting Invoices](https://docs.merge.dev/accounting/invoices/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountToken` | query | `string` | yes | Linked account token for the Merge account you want to query. The shared headers mapper sends this input as X-Account-Token. |
