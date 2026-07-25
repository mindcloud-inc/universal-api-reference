# Create Invoice with Sage Intacct

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://api.intacct.com/ia/xml/xmlgw.phtml`
- **Official documentation:** [Create Invoice](https://developer.intacct.com/api/accounts-receivable/invoices/#create-invoice-legacy)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/xml` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | body | `string` | no | — |
| `invoiceItems[].amount` | body | `number` | no | — |
| `invoiceItems[].glAccountNo` | body | `string` | no | — |
| `dateCreated` | body | `string` | no | MM/DD/YYYY |
| `invoiceItems[]` | body | `array` | no | — |
| `invoiceItems[].locationId` | body | `number` | no | — |
| `invoiceItems[].divisionId` | body | `number` | no | — |
| `invoiceNumber` | body | `string` | no | — |
| `invoiceItems[].accountLabel` | body | `string` | no | — |
| `locationId` | body | `string` | no | — |
| `divisionId` | body | `string` | no | — |
| `invoiceItems[].memo` | body | `string` | no | — |
| `externalId` | body | `string` | no | — |
| `dateDue` | body | `string` | no | MM/DD/YYYY |
| `description` | body | `string` | no | — |
| `datePosted` | body | `string` | no | — |
| `poNumber` | body | `string` | no | — |
| `customFields[]` | body | `array` | no | [{ customfieldname:"..." customfieldvalue:"testing" }] |
| `supdocId` | body | `string` | no | — |
