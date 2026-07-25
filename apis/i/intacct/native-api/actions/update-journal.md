# Update Journal with Sage Intacct

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://api.intacct.com/ia/xml/xmlgw.phtml`
- **Official documentation:** [Update Journal](https://developer.intacct.com/api/accounts-receivable/invoices/#create-invoice-legacy)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/xml` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `entries[]` | body | `array` | yes |
| `entries[].glaccount` | body | `string` | no |
| `entries[].trType` | body | `string` | no |
| `recordNo` | body | `string` | no |
| `entries[].amount` | body | `number` | no |
| `journal` | body | `string` | no |
| `batchDate` | body | `string` | no |
| `entries[].classID` | body | `string` | no |
| `batchTitle` | body | `string` | no |
| `entries[].location` | body | `string` | no |
| `entries[].itemID` | body | `string` | no |
| `entries[].description` | body | `string` | no |
