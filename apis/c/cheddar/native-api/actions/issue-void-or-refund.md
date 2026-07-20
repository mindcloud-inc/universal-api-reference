# Issue Void or Refund with Cheddar

Voids or refunds a billed invoice in Cheddar.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoices/void-or-refund/productCode/{productCode}`
- **Base URL:** `https://getcheddar.com/xml`
- **Official documentation:** [Issue Void or Refund](https://docs.getcheddar.com/#issue-a-void-or-refund)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | body | `string` | no | Cheddar-generated invoice number. Provide this or Invoice ID. |
| `id` | body | `string` | no | Cheddar invoice ID. Provide this or Invoice Number. |
| `remoteAddress` | body | `string` | no | Client IPv4 address for fraud protection and rate limiting. |
