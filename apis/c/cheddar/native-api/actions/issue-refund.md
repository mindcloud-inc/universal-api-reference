# Issue Refund with Cheddar

Creates a refund for a billed invoice in Cheddar.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoices/refund/productCode/{productCode}`
- **Base URL:** `https://getcheddar.com/xml`
- **Official documentation:** [Issue Refund](https://docs.getcheddar.com/#issue-a-refund)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | body | `string` | no | Cheddar-generated invoice number. Provide this or Invoice ID. |
| `id` | body | `string` | no | Cheddar invoice ID. Provide this or Invoice Number. |
| `amount` | body | `number` | yes | Refund amount, less than or equal to the refundable amount. |
| `remoteAddress` | body | `string` | no | Client IPv4 address for fraud protection and rate limiting. |
