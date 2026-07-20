# Issue Void with Cheddar

Voids a billed invoice transaction in Cheddar.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoices/void/productCode/{productCode}`
- **Base URL:** `https://getcheddar.com/xml`
- **Official documentation:** [Issue Void](https://docs.getcheddar.com/#issue-a-void)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | body | `string` | no | Cheddar-generated invoice number. Provide this or Invoice ID. |
| `id` | body | `string` | no | Cheddar invoice ID. Provide this or Invoice Number. |
| `remoteAddress` | body | `string` | no | Client IPv4 address for fraud protection and rate limiting. |
