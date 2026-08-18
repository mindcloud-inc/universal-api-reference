# Create Order Entry Document with Sage Intacct

Creates a new Order Entry document.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.intacct.com/ia/api/v1/objects/order-entry/document:::documentName`
- **Base URL:** `https://api.intacct.com/ia/xml/xmlgw.phtml`
- **Official documentation:** [Create Order Entry Document](https://developer.sage.com/intacct/apis/intacct/1/intacct-openapi/groups/order-entry/groups/documents/tags/order_entry_documents/paths/create-order-entry-named-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lines[].dimensions.item.id` | body | `string` | no | Unique identifier for the item.  Example: "Case 13" |
| `lines[].dimensions.location` | body | `object` | no | Location associated with the document line. |
| `lines[].dimensions.location.id` | body | `string` | no | ID for the location.  Example: "LOC-22" |
| `lines[].dimensions.warehouse` | body | `object` | no | Warehouse associated with the document line. |
| `lines[].dimensions.warehouse.id` | body | `string` | no | Unique ID for the warehouse.  Example: "WH01" |
| `lines[].unit` | body | `string` | no | Unit associated with this document line item.  Example: "Each" |
| `lines[].unitPrice` | body | `string` | no | Unit price associated with this line item.  Example: "10.50" |
| `lines[].unitQuantity` | body | `string` | no | Unit quantity associated with this document line item.  Example: "10.10" |
| `customer.id` | body | `string` | no | Unique ID for the customer.  Example: "maev co housing" |
| `documentName` | path | `string` | yes | — |
| `sourceModule` | body | `string` | yes | — |
| `txnDate` | body | `string` | yes | Date on the Order Entry document.  Example: "2024-04-04" |
| `customer` | body | `object` | no | Customer associated with the Order Entry document.  Example: "IBN" |
| `state` | body | `list<string>` | no | State of the Order Entry document.  Enum: "submitted" "approved" "partiallyApproved" "declined" "draft" "pending" "closed" "inProgress" "converted" "partiallyConverted" "convertedByLine" "partiallyConvertedByLine" "exception"  Default: "pending" |
| `dueDate` | body | `string` | no | Due date for the Order Entry document.  Example: "2024-04-04" |
| `txnCurrency` | body | `string` | no | Currency used for the transaction.  Example: "USD" |
| `baseCurrency` | body | `string` | no | Base currency for the transaction.  Example: "USD" |
| `lines[]` | body | `array` | no | Lines of the Order Entry document. |
| `lines[].dimensions` | body | `object` | no | — |
| `lines[].dimensions.item` | body | `object` | no | — |
