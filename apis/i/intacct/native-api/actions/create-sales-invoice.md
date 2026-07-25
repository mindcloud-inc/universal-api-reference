# Create Sales Invoice with Sage Intacct

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://api.intacct.com/ia/xml/xmlgw.phtml`
- **Official documentation:** [Create Sales Invoice](https://developer.intacct.com/api/accounts-receivable/invoices/#create-invoice-legacy)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/xml` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | body | `string` | no | — |
| `customFields[].name` | body | `string` | no | — |
| `invoiceItems[].itemId` | body | `string` | no | — |
| `customFields[].value` | body | `string` | no | — |
| `dateCreated` | body | `string` | no | — |
| `invoiceItems[].price` | body | `number` | no | — |
| `invoiceItems[]` | body | `array` | no | — |
| `documentNumber` | body | `string` | no | — |
| `invoiceItems[].locationId` | body | `string` | no | — |
| `invoiceItems[].divisionId` | body | `string` | no | — |
| `invoiceItems[].quantity` | body | `number` | no | — |
| `message` | body | `string` | no | — |
| `entityID` | body | `string` | no | — |
| `invoiceItems[].description` | body | `string` | no | — |
| `state` | body | `string` | no | Draft \| Pending \| Closed |
| `referenceNumber` | body | `string` | no | — |
| `customFields[]` | body | `array<object>` | no | — |
| `customerPONumber` | body | `string` | no | — |
