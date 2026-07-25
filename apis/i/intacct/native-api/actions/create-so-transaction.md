# Create So Transaction with Sage Intacct

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.intacct.com/ia/xml/xmlgw.phtml`
- **Base URL:** `https://api.intacct.com/ia/xml/xmlgw.phtml`
- **Official documentation:** [Create So Transaction](https://developer.intacct.com/api/order-entry/order-entry-transactions/#create-order-entry-transaction-legacy)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `newfields[].fieldName` | body | `string` | no |
| `newfields[].internalFields[].fieldValue` | body | `string` | no |
| `transactiontype` | body | `string` | yes |
| `fields` | body | `string<object>` | yes |
| `newfields[].fieldValue` | body | `string` | no |
| `newfields[].internalFields[].fieldName` | body | `string` | no |
| `entityID` | body | `string` | no |
| `newfields[].fieldIterator` | body | `string` | no |
| `newfields[].internalFields[]` | body | `array<object>` | no |
