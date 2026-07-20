# Update Invoice with CoachAccountable

Updates an invoice in CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Update Invoice](https://www.coachaccountable.com/APIDocs#Invoice.update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `InvoiceID` | body | `number` | yes | The ID of the Invoice to be updated. Invoice Number also accepted when prefixed with a "#", e.g. "#1005". |
| `dateOf` | body | `date` | no | A new date of the Invoice, if it is to be changed. |
| `number` | body | `string` | no | A new number for the Invoice, if it is to be changed. Maximum length: 20. |
| `taxRate` | body | `number` | no | A percentage-based rate of tax to be applied, e.g. 7.5 means apply a 7.5% tax. |
| `lineItemSet` | body | `string` | no | A newline-separated list of items. An item is comprised of the item label followed by a double colon followed by the price. For example: "One month of coaching::400" |
