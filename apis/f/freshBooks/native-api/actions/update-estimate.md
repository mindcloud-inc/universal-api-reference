# Update Estimate with FreshBooks

Updates an existing estimate in FreshBooks for an account.

## Endpoint

- **Method:** `PUT`
- **Path:** `/accounting/account/:accountId/estimates/estimates/:estimateId`
- **Base URL:** `https://api.freshbooks.com`
- **Official documentation:** [Update Estimate](https://www.freshbooks.com/api/estimates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | FreshBooks accounting account ID. |
| `estimateId` | path | `string` | yes | FreshBooks estimate ID. |
| `estimate.customerid` | body | `number` | no | — |
| `estimate.create_date` | body | `string` | no | — |
| `estimate.notes` | body | `string` | no | — |
| `estimate.lines[].name` | body | `string` | no | — |
| `estimate.lines[].qty` | body | `number` | no | — |
| `estimate.lines[].unit_cost.amount` | body | `string` | no | — |
| `estimate.lines[].unit_cost.code` | body | `string` | no | — |
