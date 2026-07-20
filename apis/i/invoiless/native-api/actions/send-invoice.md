# Send Invoice with Invoiless

Sends an invoice to a customer in Invoiless.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoices/:id/send`
- **Base URL:** `https://api.invoiless.com/v1`
- **Official documentation:** [Send Invoice](https://docs.invoiless.com/guide/invoices.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Invoice id. |
| `email` | body | `string` | no | Email address. |
| `subject` | body | `string` | no | Email subject. |
| `body` | body | `string` | no | Email body. |
| `date` | body | `date` | no | Schedule send date. |
