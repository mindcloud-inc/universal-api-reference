# Send Invoice to Client with Envoice

Sends an invoice to a client in Envoice.

## Endpoint

- **Method:** `POST`
- **Path:** `invoice/sendtoclient`
- **Base URL:** `https://www.envoice.in/api`
- **Official documentation:** [Send Invoice to Client](https://github.com/EmitKnowledge/Envoice/blob/master/invoice.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `InvoiceId` | body | `number` | yes | Invoice ID. |
| `Message` | body | `string` | yes | Email message sent with the invoice. |
