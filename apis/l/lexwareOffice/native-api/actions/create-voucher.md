# Create Voucher with Lexware Office

Creates a new voucher in Lexware Office.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/vouchers`
- **Base URL:** `https://api.lexware.io`
- **Official documentation:** [Create Voucher](https://developers.lexware.io/docs/#vouchers-endpoint-create-a-voucher)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Voucher type, for example expenseinvoice or salesinvoice. |
| `voucherStatus` | body | `string` | no | Set unchecked for draft bookkeeping vouchers. |
| `voucherNumber` | body | `string` | no | Voucher number; required unless status is unchecked. |
| `voucherDate` | body | `date` | no | Voucher date in RFC 3339 format. |
| `shippingDate` | body | `date` | no | Optional shipping date in RFC 3339 format. |
| `dueDate` | body | `date` | no | Optional due date in RFC 3339 format. |
| `totalGrossAmount` | body | `number` | no | Total gross amount; required unless status is unchecked. |
| `totalTaxAmount` | body | `number` | no | Total tax amount; required unless status is unchecked. |
| `taxType` | body | `string` | yes | Tax type, for example gross or net. |
| `useCollectiveContact` | body | `boolean` | no | Use the Lexware collective contact instead of contactId. |
| `contactId` | body | `string` | no | Existing contact ID when not using the collective contact. |
| `voucherItems[]` | body | `array<object>` | no | Array of voucher item objects. |
| `version` | body | `number` | no | Optional version on create; must be 1 if provided. |
