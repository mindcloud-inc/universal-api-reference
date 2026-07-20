# Send or Resend Invoice Email with Cheddar

Sends or resends an invoice email in Cheddar.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoices/send-email/productCode/{productCode}`
- **Base URL:** `https://getcheddar.com/xml`
- **Official documentation:** [Send or Resend Invoice Email](https://docs.getcheddar.com/#send-or-resend-an-invoice-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | body | `string` | no | Cheddar-generated invoice number. Provide this or Invoice ID. |
| `id` | body | `string` | no | Cheddar invoice ID. Provide this or Invoice Number. |
| `remoteAddress` | body | `string` | no | Client IPv4 address for fraud protection and rate limiting. |
