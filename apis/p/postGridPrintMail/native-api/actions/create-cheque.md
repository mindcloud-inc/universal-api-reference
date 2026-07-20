# Create Cheque with PostGrid Print & Mail

Creates a cheque in PostGrid Print & Mail.

## Endpoint

- **Method:** `POST`
- **Path:** `/cheques`
- **Base URL:** `https://api.postgrid.com/print-mail/v1`
- **Official documentation:** [Create Cheque](https://postgrid.readme.io/reference/cheques_create-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `to` | body | `string` | yes | The recipient contact ID or recipient payload. |
| `from` | body | `string` | yes | The sender contact ID or sender payload. |
| `bankAccount` | body | `string` | yes | The PostGrid bank account ID to use for the cheque. |
| `amount` | body | `number` | yes | The cheque amount in the smallest currency unit. |
| `mergeVariables` | body | `object` | no | Template merge variables for the cheque. |
| `description` | body | `string` | no | An optional description visible in the API and dashboard. |
| `metadata` | body | `object` | no | Custom metadata for this cheque. |
| `sendDate` | body | `date` | no | Schedule the cheque for a future send date. |
| `mailingClass` | body | `string` | no | The mailing class for the cheque. |
| `memo` | body | `string` | no | The memo text for the cheque. |
| `message` | body | `string` | no | The message body for the cheque. |
| `logoURL` | body | `string` | no | A logo URL to print on the cheque. |
| `number` | body | `number` | no | The cheque number. |
| `envelope` | body | `string` | no | Envelope settings for the cheque. |
| `digitalOnly` | body | `object` | no | Digital delivery settings for the cheque. |
| `redirectTo` | body | `string` | no | A redirected recipient contact ID or payload. |
| `size` | body | `string` | no | The cheque paper size. |
| `currencyCode` | body | `string` | no | The currency code for the cheque amount. |
