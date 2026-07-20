# Create Customer with Invoiless

Creates a new customer in Invoiless.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers`
- **Base URL:** `https://api.invoiless.com/v1`
- **Official documentation:** [Create Customer](https://docs.invoiless.com/guide/customers.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `billTo` | body | `object` | yes | Billing address object. Either firstName and lastName, or company, is required inside this object. |
| `shipTo` | body | `object` | no | Shipping address object. |
| `cc[]` | body | `array<string>` | no | Cc recipients. |
| `bcc[]` | body | `array<string>` | no | Bcc recipients. |
| `currency` | body | `string` | no | ISO 4217 currency code. |
| `lang` | body | `string` | no | Customer language code. |
| `dateFormat` | body | `string` | no | Preferred date format. |
| `attachPdf` | body | `boolean` | no | Attach a PDF copy to emails. |
| `notes` | body | `string` | no | Private notes. |
| `tags[]` | body | `array<string>` | no | Tags. |
