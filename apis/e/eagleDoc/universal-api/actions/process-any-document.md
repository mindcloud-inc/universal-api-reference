# Eagle Doc: Process Any Document

Creates an any-document extraction in Eagle Doc.

```
POST https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/process-any-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eagle Doc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/process-any-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/process-any-document', {
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
| `configId` | string | no | Optional Eagle Doc custom extraction configuration ID |
| `docType` | string | no | Known Eagle Doc document type for more stable extraction |
| `file` | file | yes | Document file to upload |
| `privacy` | boolean | no | Whether Eagle Doc should avoid storing the uploaded file |

## Response

```json
{
  "success": true,
  "data": [
    {
      "docType": "string",
      "general": {
        "category": "string",
        "currency": "string",
        "customerCity": "string",
        "customerCountry": "string",
        "customerName": "Ava Chen",
        "customerStreet": "string",
        "customerZip": "string",
        "documentType": "string",
        "email": "ava@example.com",
        "invoiceDate": "2026-05-07T12:00:00.000Z",
        "invoiceDueDate": "2026-05-07T12:00:00.000Z",
        "invoiceNumber": "string",
        "orderNumber": "string",
        "reverseCharge": true,
        "shopCity": "string",
        "shopCountry": "string",
        "shopName": "Ava Chen",
        "shopStreet": "string",
        "shopZip": "string",
        "taxAmount": 1,
        "taxGrossAmount": 1,
        "taxNetAmount": 1,
        "taxPercentage": 1,
        "totalPrice": 1
      },
      "lists": {
        "productItems": [
          {
            "currency": "string",
            "productName": "Ava Chen",
            "productPrice": 1,
            "productQuantity": 1,
            "productUnitPrice": 1,
            "taxAmount": 1,
            "taxGrossAmount": 1,
            "taxNetAmount": 1,
            "taxPercentage": 1
          }
        ],
        "taxes": [
          {
            "taxAmount": 1,
            "taxGrossAmount": 1,
            "taxNetAmount": 1,
            "taxPercentage": 1
          }
        ]
      },
      "processingInfo": {
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
        },
        "productsSumVsTotalPrice": {
          "flagValid": true,
          "message": "string"
        },
        "taxPercentage": {
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
| `general.category` | string |  |
| `general.currency` | string |  |
| `general.customerCity` | string |  |
| `general.customerCountry` | string |  |
| `general.customerName` | string |  |
| `general.customerStreet` | string |  |
| `general.customerZip` | string |  |
| `general.documentType` | string |  |
| `general.email` | string |  |
| `general.invoiceDate` | date |  |
| `general.invoiceDueDate` | date |  |
| `general.invoiceNumber` | string |  |
| `general.orderNumber` | string |  |
| `general.reverseCharge` | boolean |  |
| `general.shopCity` | string |  |
| `general.shopCountry` | string |  |
| `general.shopName` | string |  |
| `general.shopStreet` | string |  |
| `general.shopZip` | string |  |
| `general.taxAmount` | number |  |
| `general.taxGrossAmount` | number |  |
| `general.taxNetAmount` | number |  |
| `general.taxPercentage` | number |  |
| `general.totalPrice` | number |  |
| `lists.productItems[].currency` | string |  |
| `lists.productItems[].productName` | string |  |
| `lists.productItems[].productPrice` | number |  |
| `lists.productItems[].productQuantity` | number |  |
| `lists.productItems[].productUnitPrice` | number |  |
| `lists.productItems[].taxAmount` | number |  |
| `lists.productItems[].taxGrossAmount` | number |  |
| `lists.productItems[].taxNetAmount` | number |  |
| `lists.productItems[].taxPercentage` | number |  |
| `lists.taxes[].taxAmount` | number |  |
| `lists.taxes[].taxGrossAmount` | number |  |
| `lists.taxes[].taxNetAmount` | number |  |
| `lists.taxes[].taxPercentage` | number |  |
| `processingInfo.docType` | string |  |
| `processingInfo.duration` | string |  |
| `processingInfo.fileHash` | string |  |
| `processingInfo.language` | string |  |
| `processingInfo.numberOfPages` | string |  |
| `processingInfo.version` | string |  |
| `signatures` | object |  |
| `verification.nonDuplication.flagValid` | boolean |  |
| `verification.nonDuplication.message` | string |  |
| `verification.productsSumVsTotalPrice.flagValid` | boolean |  |
| `verification.productsSumVsTotalPrice.message` | string |  |
| `verification.taxPercentage.flagValid` | boolean |  |
| `verification.taxPercentage.message` | string |  |

## Native endpoint

Through the native Eagle Doc API, this operation is `POST /api/anydoc/v1/processing` (base URL `https://de.eagle-doc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/process-any-document.md) for the provider-specific parameters and requirements.

