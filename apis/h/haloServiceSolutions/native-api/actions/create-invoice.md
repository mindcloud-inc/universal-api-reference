# Create Invoice with Halo Service Solutions

Creates a new invoice in Halo Service Solutions.

## Endpoint

- **Method:** `POST`
- **Path:** `/Invoice`
- **Base URL:** `https://mindcloud.halopsa.com/api`
- **Official documentation:** [Create Invoice](https://usehalo.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `[]` | body | `array<object>` | no | Invoice payload array. |
| `[].invoice_date` | body | `string` | no | Date invoiced. |
| `[].name` | body | `string` | no | Invoice name. |
| `[].client_id` | body | `number` | no | Client ID for the invoice. |
| `[].sitenumber` | body | `number` | no | Site number for the invoice. |
| `[].uid` | body | `number` | no | User ID for the invoice. |
| `[].assigned_agent` | body | `number` | no | Assigned agent ID for the invoice. |
| `[].add_salesorder` | body | `number` | no | Existing sales order to invoice from. |
| `[].internal_note` | body | `string` | no | Internal note for the invoice. |
