# Create So Transaction with Sage Intacct

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.intacct.com/ia/xml/xmlgw.phtml`
- **Base URL:** `https://api.intacct.com/ia/xml/xmlgw.phtml`
- **Official documentation:** [Create So Transaction](https://developer.intacct.com/api/order-entry/order-entry-transactions/#create-order-entry-transaction-legacy)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `fields[].fieldName` | body | `string` | no |
| `fields[].internalFields[].fieldValue` | body | `string` | no |
| `transactiontype` | body | `string` | yes |
| `fields[]` | body | `array<object>` | yes |
| `fields[].fieldValue` | body | `string` | no |
| `fields[].internalFields[].fieldName` | body | `string` | no |
| `entityID` | body | `string` | no |
| `fields[].fieldIterator` | body | `string` | no |
| `fields[].internalFields[]` | body | `array<object>` | no |
