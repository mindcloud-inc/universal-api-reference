# List Invoices with Billwerkplus

Retrieves invoices from Billwerkplus.

## Endpoint

- **Method:** `GET`
- **Path:** `/list/invoice`
- **Base URL:** `https://api.frisbii.com/v1`
- **Official documentation:** [List Invoices](https://docs.frisbii.com/reference/getinvoicelist)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `date` | no | Inclusive start of the local account time range. |
| `to` | query | `date` | no | Exclusive end of the local account time range. |
| `interval` | query | `string` | no | ISO 8601 duration counted back from To. |
| `range` | query | `list` | no | Time attribute to limit by: created or settled. Accepted values: `0`, `1`. |
| `handle` | query | `string` | no | Exact invoice handle. |
| `handle_prefix` | query | `string` | no | Invoice handle prefix. |
| `handle_contains` | query | `string` | no | Invoice handle contains filter. |
| `state[]` | query | `array<string>` | no | Invoice states to include. Multiple values are allowed. Send multiple values as a array. |
| `customer` | query | `string` | no | Customer handle filter. |
| `currency[]` | query | `array<string>` | no | Invoice currency filter. Multiple values are allowed. Send multiple values as a array. |
| `type[]` | query | `array<string>` | no | Invoice types to include. Multiple values are allowed. Send multiple values as a array. |
| `subscription` | query | `string` | no | Subscription handle filter. |
| `plan` | query | `string` | no | Subscription plan handle filter. |
| `due` | query | `date` | no | Due date filter. |
