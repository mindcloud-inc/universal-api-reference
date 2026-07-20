# Update Voucher with Lexware Office

Updates an existing voucher in Lexware Office.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/vouchers/:id`
- **Base URL:** `https://api.lexware.io`
- **Official documentation:** [Update Voucher](https://developers.lexware.io/docs/#vouchers-endpoint-update-a-voucher)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Voucher ID from Lexware. |
| `type` | body | `string` | yes | Voucher type. |
| `voucherStatus` | body | `string` | no | Voucher status. |
| `voucherNumber` | body | `string` | no | Voucher number. |
| `voucherDate` | body | `date` | no | Voucher date. |
| `shippingDate` | body | `date` | no | Shipping date. |
| `dueDate` | body | `date` | no | Due date. |
| `totalGrossAmount` | body | `number` | no | Total gross amount. |
| `totalTaxAmount` | body | `number` | no | Total tax amount. |
| `taxType` | body | `string` | yes | Tax type. |
| `useCollectiveContact` | body | `boolean` | no | Use the collective contact. |
| `contactId` | body | `string` | no | Existing contact ID. |
| `voucherItems[]` | body | `array<object>` | no | Array of voucher item objects. |
| `version` | body | `number` | yes | Current voucher version from Lexware. |
