# Create Invoice with Envoice

Creates a new invoice in Envoice.

## Endpoint

- **Method:** `POST`
- **Path:** `invoice/new`
- **Base URL:** `https://www.envoice.in/api`
- **Official documentation:** [Create Invoice](https://github.com/EmitKnowledge/Envoice/blob/master/invoice.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientId` | body | `number` | yes | Envoice client identifier for the invoice. |
| `Number` | body | `string` | yes | Invoice number to assign in Envoice. |
| `IssuedOn` | body | `date` | yes | Invoice issue date. |
| `Duedate` | body | `date` | yes | Invoice due date. Envoice expects the field name Duedate. |
| `Status` | body | `string` | yes | Invoice status value accepted by Envoice, such as Draft. |
| `CurrencyId` | body | `number` | yes | Currency identifier for the invoice. |
| `PaymentGateways` | body | `string<object>` | yes | Payment gateway JSON array accepted by Envoice, for example [{"Name":"paypal"}]. |
| `Items` | body | `string<object>` | yes | Invoice line items JSON array accepted by Envoice with WorkTypeId, Description, Cost, Quantity, and TaxId. |
