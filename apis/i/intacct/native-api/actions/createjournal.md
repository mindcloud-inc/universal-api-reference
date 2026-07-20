# Create Journal with Sage Intacct

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://api.intacct.com/ia/xml/xmlgw.phtml`
- **Official documentation:** [Create Journal](https://developer.intacct.com/api/accounts-receivable/invoices/#create-invoice-legacy)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/xml` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `entries[].department` | body | `string` | no |
| `journal` | body | `string` | yes |
| `batchDate` | body | `string` | yes |
| `entries[].glaccount` | body | `string` | no |
| `batchTitle` | body | `string` | yes |
| `entries[].trType` | body | `string` | no |
| `entries[]` | body | `array` | yes |
| `entries[].amount` | body | `number` | no |
| `entries[].classID` | body | `string` | no |
| `entries[].location` | body | `string` | no |
| `entries[].itemID` | body | `string` | no |
| `entries[].description` | body | `string` | no |
