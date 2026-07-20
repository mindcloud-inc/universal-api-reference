# Eagle Doc: Parse Delivery Sheet

Creates a delivery sheet extraction in Eagle Doc.

```
POST https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/parse-delivery-sheet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eagle Doc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/parse-delivery-sheet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/parse-delivery-sheet', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | Delivery sheet file to upload |

## Response

```json
{
  "success": true,
  "data": [
    {
      "docType": "string",
      "general": {
        "additionalNotes": "string",
        "customerAddress": "string",
        "customerEmail": "ava@example.com",
        "customerName": "Ava Chen",
        "deliveryDate": "2026-05-07T12:00:00.000Z",
        "deliveryLocation": "string",
        "deliveryPerson": "string",
        "documentNumber": "string",
        "invoiceDate": "2026-05-07T12:00:00.000Z",
        "invoiceNumber": "string",
        "issueDate": "2026-05-07T12:00:00.000Z",
        "paymentTerms": "string",
        "purchaseOrderNumber": "string",
        "receiverName": "Ava Chen",
        "shippingMethod": "string",
        "supplierAddress": "string",
        "supplierCity": "string",
        "supplierEmail": "ava@example.com",
        "supplierName": "Ava Chen",
        "supplierState": "string",
        "supplierStreet": "string",
        "supplierZipCode": "string"
      },
      "lists": {
        "productList": [
          {
            "productId": "string",
            "productName": "Ava Chen",
            "productQuantity": "string"
          }
        ]
      },
      "processingInfo": {
        "docConfigId": {},
        "docType": "string",
        "duration": "string",
        "fileHash": "string",
        "language": "string",
        "numberOfPages": "string",
        "version": "string"
      },
      "signatures": {},
      "verification": {
        "nonDuplication": {
          "flagValid": true,
          "message": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `docType` | string |  |
| `general.additionalNotes` | string |  |
| `general.customerAddress` | string |  |
| `general.customerEmail` | string |  |
| `general.customerName` | string |  |
| `general.deliveryDate` | date |  |
| `general.deliveryLocation` | string |  |
| `general.deliveryPerson` | string |  |
| `general.documentNumber` | string |  |
| `general.invoiceDate` | date |  |
| `general.invoiceNumber` | string |  |
| `general.issueDate` | date |  |
| `general.paymentTerms` | string |  |
| `general.purchaseOrderNumber` | string |  |
| `general.receiverName` | string |  |
| `general.shippingMethod` | string |  |
| `general.supplierAddress` | string |  |
| `general.supplierCity` | string |  |
| `general.supplierEmail` | string |  |
| `general.supplierName` | string |  |
| `general.supplierState` | string |  |
| `general.supplierStreet` | string |  |
| `general.supplierZipCode` | string |  |
| `lists.productList[].productId` | string |  |
| `lists.productList[].productName` | string |  |
| `lists.productList[].productQuantity` | string |  |
| `processingInfo.docConfigId` | object |  |
| `processingInfo.docType` | string |  |
| `processingInfo.duration` | string |  |
| `processingInfo.fileHash` | string |  |
| `processingInfo.language` | string |  |
| `processingInfo.numberOfPages` | string |  |
| `processingInfo.version` | string |  |
| `signatures` | object |  |
| `verification.nonDuplication.flagValid` | boolean |  |
| `verification.nonDuplication.message` | string |  |

## Native endpoint

Through the native Eagle Doc API, this operation is `POST /api/anydoc/v1/processing` (base URL `https://de.eagle-doc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/parse-delivery-sheet.md) for the provider-specific parameters and requirements.

