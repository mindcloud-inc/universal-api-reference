# Send Invoice Email with Alegra

Sends a sales invoice by email from Alegra.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoices/:id/email`
- **Base URL:** `https://api.alegra.com/api/v1`
- **Official documentation:** [Send Invoice Email](https://developer.alegra.com/reference/post_invoices-id-email)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `emails[]` | body | `array<string>` | yes |
| `sendCopyToUser` | body | `boolean` | no |
| `invoiceType` | body | `string` | no |
| `emailMessage.subject` | body | `string` | no |
