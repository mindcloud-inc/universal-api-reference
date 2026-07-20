# Create Estimate with FreshBooks

Creates a new estimate in FreshBooks for an account.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounting/account/:accountId/estimates/estimates`
- **Base URL:** `https://api.freshbooks.com`
- **Official documentation:** [Create Estimate](https://www.freshbooks.com/api/estimates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | FreshBooks accounting account ID. |
| `estimate.customerid` | body | `number` | yes | — |
| `estimate.create_date` | body | `string` | yes | — |
| `estimate.notes` | body | `string` | no | — |
| `estimate.lines[].name` | body | `string` | yes | — |
| `estimate.lines[].qty` | body | `number` | yes | — |
| `estimate.lines[].unit_cost.amount` | body | `string` | yes | — |
| `estimate.lines[].unit_cost.code` | body | `string` | yes | — |
