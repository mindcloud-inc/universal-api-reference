# Record Invoice Payment with CoachAccountable

Records an invoice payment in CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Record Invoice Payment](https://www.coachaccountable.com/APIDocs#Invoice.addPayment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `InvoiceID` | body | `number` | yes | The ID of the Invoice to which the record of payment is to be added. Invoice Number also accepted when prefixed with a "#", e.g. "#1005". |
| `dateOf` | body | `date` | no | Will fill in as the current time when not supplied. Future dates not allowed. |
| `amount` | body | `number` | yes | — |
| `method` | body | `list` | no | If not supplied, will assume "Credit Card" Accepted values: `Bank Transfer`, `Cash`, `Check`, `Credit Card`, `Other`. |
| `checkNumber` | body | `string` | no | Optional memo that will be saved when supplied and method="Check" Maximum length: 20. |
| `allowOverpay` | body | `boolean` | no | If not set to "true", will throw an error if the added payment results in a net overpay of the invoice. |
