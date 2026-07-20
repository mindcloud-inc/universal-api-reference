# Update Invoice with Invoiless

Updates an existing invoice in Invoiless.

## Endpoint

- **Method:** `PUT`
- **Path:** `/invoices/:id`
- **Base URL:** `https://api.invoiless.com/v1`
- **Official documentation:** [Update Invoice](https://docs.invoiless.com/guide/invoices.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Invoice id. |
| `customer` | body | `string` | no | Customer id. The Invoiless docs also allow an object here, but this draft currently standardizes on a customer id string. |
| `items[]` | body | `array<object>` | no | Invoice line items array. |
| `number` | body | `string` | no | Invoice number. |
| `date` | body | `date` | no | Invoice date. |
| `dueDate` | body | `date` | no | Invoice due date. |
| `currency` | body | `string` | no | ISO 4217 currency code. |
| `lang` | body | `string` | no | Invoice language code. |
| `status` | body | `string` | no | Invoice status. |
| `terms` | body | `string` | no | Invoice terms. |
| `notes` | body | `string` | no | Invoice notes. |
| `tags[]` | body | `array<string>` | no | Invoice tags. |
| `taxIncluded` | body | `boolean` | no | Whether tax is included in prices. |
