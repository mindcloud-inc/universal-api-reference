# Create Invoice with CoachAccountable

Creates an invoice in CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Create Invoice](https://www.coachaccountable.com/APIDocs#Invoice.add)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientID` | body | `number` | no | The ID of the Client for whom this invoice is (if not for a Company). |
| `CompanyID` | body | `number` | no | The ID of the Company for whom this invoice is (if not for a Client). |
| `dateOf` | body | `date` | yes | — |
| `dateDue` | body | `date` | no | If omitted, the due date will be calculated based on the dateOf and your setting of how many days out invoices are due by default. |
| `number` | body | `string` | no | If not supplied, a logical next invoice number will be assigned. Letters are allowed, e.g. "A1002". Maximum length: 20. |
| `taxRate` | body | `number` | no | A percentage-based rate of tax to be applied, e.g. 7.5 means apply a 7.5% tax. |
| `onDuplicateNumber` | body | `list` | no | What to do if an Invoice with the supplied number already exists. Accepted values: `A`, `E`, `S`. |
| `currency` | body | `string` | no | The ISO 4217 3-letter code of the currency. If not supplied, or not among the chosen accepted currencies, the chosen primary currency will be assumed. Maximum length: 3. |
| `lineItemSet` | body | `string` | no | A newline-separated list of items. An item is comprised of the item label followed by a double colon followed by the price. For example: "One month of coaching::400" |
| `collectPaymentIfPossible` | body | `boolean` | no | If set to "true", will try to collect full payment for the invoice immediately (using a client's card on file). To determine if the charge was successful, use Invoice.get. |
