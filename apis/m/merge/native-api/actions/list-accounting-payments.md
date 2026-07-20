# List Accounting Payments with Merge

## Endpoint

- **Method:** `GET`
- **Path:** `/api/accounting/v1/payments`
- **Base URL:** `https://api.merge.dev`
- **Official documentation:** [List Accounting Payments](https://docs.merge.dev/accounting/payments/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountToken` | query | `string` | yes | Linked account token for the Merge account you want to query. The shared headers mapper sends this input as X-Account-Token. |
