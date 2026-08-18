# Sage Intacct: Create Order Entry Document

Creates a new Order Entry document.

```
POST https://connect.mindcloud.co/v1/universal/intacct/latest/actions/create-order-entry-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sage Intacct `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intacct/latest/actions/create-order-entry-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentName": "Ava Chen",
  "sourceModule": "orderEntry",
  "txnDate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intacct/latest/actions/create-order-entry-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentName": "Ava Chen",
    "sourceModule": "orderEntry",
    "txnDate": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `lines[].dimensions.item.id` | string | no | Unique identifier for the item. Example: "Case 13" |
| `lines[].dimensions.location` | object | no | Location associated with the document line. |
| `lines[].dimensions.location.id` | string | no | ID for the location. Example: "LOC-22" |
| `lines[].dimensions.warehouse` | object | no | Warehouse associated with the document line. |
| `lines[].dimensions.warehouse.id` | string | no | Unique ID for the warehouse. Example: "WH01" |
| `lines[].unit` | string | no | Unit associated with this document line item. Example: "Each" |
| `lines[].unitPrice` | string | no | Unit price associated with this line item. Example: "10.50" |
| `lines[].unitQuantity` | string | no | Unit quantity associated with this document line item. Example: "10.10" |
| `customer.id` | string | no | Unique ID for the customer. Example: "maev co housing" |
| `documentName` | string | yes |  |
| `sourceModule` | string | yes | Example: `orderEntry`. |
| `txnDate` | string | yes | Date on the Order Entry document. Example: "2024-04-04" |
| `customer` | object | no | Customer associated with the Order Entry document. Example: "IBN" |
| `state` | list<string> | no | State of the Order Entry document. Enum: "submitted" "approved" "partiallyApproved" "declined" "draft" "pending" "closed" "inProgress" "converted" "partiallyConverted" "convertedByLine" "partiallyConvertedByLine" "exception" Default: "pending" |
| `dueDate` | string | no | Due date for the Order Entry document. Example: "2024-04-04" |
| `txnCurrency` | string | no | Currency used for the transaction. Example: "USD" |
| `baseCurrency` | string | no | Base currency for the transaction. Example: "USD" |
| `lines[]` | array | no | Lines of the Order Entry document. |
| `lines[].dimensions` | object | no |  |
| `lines[].dimensions.item` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sage Intacct API returns.

## Native endpoint

Through the native Sage Intacct API, this operation is `POST https://api.intacct.com/ia/api/v1/objects/order-entry/document:::documentName` (base URL `https://api.intacct.com/ia/xml/xmlgw.phtml`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order-entry-document.md) for the provider-specific parameters and requirements.

