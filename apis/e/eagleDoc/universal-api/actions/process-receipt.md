# Eagle Doc: Process Receipt

Creates a receipt extraction in Eagle Doc.

```
POST https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/process-receipt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eagle Doc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/process-receipt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/process-receipt', {
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
| `file` | file | yes | Receipt file to upload |
| `fullText` | boolean | no | Include the extracted full text by page |
| `polygon` | boolean | no | Include polygon coordinates in the response |
| `privacy` | boolean | no | Whether Eagle Doc should avoid storing the uploaded file |
| `speed` | boolean | no | Prefer faster processing over higher accuracy |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fileHash": "string",
      "fullText": {},
      "general": {
        "category": {
          "confidence": 1,
          "value": "string"
        },
        "currency": {
          "confidence": 1,
          "value": "string"
        },
        "invoiceDate": {
          "confidence": 1,
          "page": 1,
          "value": "2026-05-07T12:00:00.000Z"
        },
        "invoiceNumber": {
          "confidence": 1,
          "page": 1,
          "value": "string"
        },
        "paymentMethod": {
          "confidence": 1,
          "value": "string"
        },
        "shopCountry": {
          "confidence": 1,
          "page": 1,
          "value": "string"
        },
        "shopName": {
          "confidence": 1,
          "page": 1,
          "value": "Ava Chen"
        },
        "shopStreet": {
          "confidence": 1,
          "page": 1,
          "value": "string"
        },
        "time": {
          "confidence": 1,
          "page": 1,
          "value": "2026-05-07T12:00:00.000Z"
        },
        "totalPrice": {
          "confidence": 1,
          "page": 1,
          "value": "string"
        },
        "vATNumber": {
          "confidence": 1,
          "page": 1,
          "value": "string"
        }
      },
      "languages": [
        "string"
      ],
      "mainLanguage": "string",
      "numberOfPages": 1,
      "pages": [
        {
          "height": 1,
          "width": 1
        }
      ],
      "payments": [
        {
          "paymentMethod": {
            "confidence": 1,
            "page": 1,
            "value": "string"
          }
        }
      ],
      "performanceOption": "string",
      "productItems": [
        {
          "currency": {
            "confidence": 1,
            "value": "string"
          },
          "productName": {
            "confidence": 1,
            "page": 1,
            "value": "Ava Chen"
          },
          "productPrice": {
            "confidence": 1,
            "page": 1,
            "value": "string"
          }
        }
      ],
      "taxes": {},
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
      },
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fileHash` | string |  |
| `fullText` | object |  |
| `general.category.confidence` | number |  |
| `general.category.value` | string |  |
| `general.currency.confidence` | number |  |
| `general.currency.value` | string |  |
| `general.invoiceDate.confidence` | number |  |
| `general.invoiceDate.page` | number |  |
| `general.invoiceDate.value` | date |  |
| `general.invoiceNumber.confidence` | number |  |
| `general.invoiceNumber.page` | number |  |
| `general.invoiceNumber.value` | string |  |
| `general.paymentMethod.confidence` | number |  |
| `general.paymentMethod.value` | string |  |
| `general.shopCountry.confidence` | number |  |
| `general.shopCountry.page` | number |  |
| `general.shopCountry.value` | string |  |
| `general.shopName.confidence` | number |  |
| `general.shopName.page` | number |  |
| `general.shopName.value` | string |  |
| `general.shopStreet.confidence` | number |  |
| `general.shopStreet.page` | number |  |
| `general.shopStreet.value` | string |  |
| `general.time.confidence` | number |  |
| `general.time.page` | number |  |
| `general.time.value` | date |  |
| `general.totalPrice.confidence` | number |  |
| `general.totalPrice.page` | number |  |
| `general.totalPrice.value` | string |  |
| `general.vATNumber.confidence` | number |  |
| `general.vATNumber.page` | number |  |
| `general.vATNumber.value` | string |  |
| `languages[]` | string |  |
| `mainLanguage` | string |  |
| `numberOfPages` | number |  |
| `pages[].height` | number |  |
| `pages[].width` | number |  |
| `payments[].paymentMethod.confidence` | number |  |
| `payments[].paymentMethod.page` | number |  |
| `payments[].paymentMethod.value` | string |  |
| `performanceOption` | string |  |
| `productItems[].currency.confidence` | number |  |
| `productItems[].currency.value` | string |  |
| `productItems[].productName.confidence` | number |  |
| `productItems[].productName.page` | number |  |
| `productItems[].productName.value` | string |  |
| `productItems[].productPrice.confidence` | number |  |
| `productItems[].productPrice.page` | number |  |
| `productItems[].productPrice.value` | string |  |
| `taxes` | object |  |
| `verification.nonDuplication.flagValid` | boolean |  |
| `verification.nonDuplication.message` | string |  |
| `verification.productsSumVsTotalPrice.flagValid` | boolean |  |
| `verification.productsSumVsTotalPrice.message` | string |  |
| `verification.taxPercentage.flagValid` | boolean |  |
| `verification.taxPercentage.message` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Eagle Doc API, this operation is `POST /api/receipt/v3/processing` (base URL `https://de.eagle-doc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/process-receipt.md) for the provider-specific parameters and requirements.

