# Eagle Doc: Process Finance Document

Creates a finance document extraction in Eagle Doc.

```
POST https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/process-finance-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eagle Doc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/process-finance-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/process-finance-document', {
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
| `file` | file | yes | Receipt or invoice file to upload |
| `fullText` | boolean | no | Include the extracted full text by page |
| `polygon` | boolean | no | Include polygon coordinates in the response |
| `privacy` | boolean | no | Whether Eagle Doc should avoid storing the uploaded file |
| `signature` | boolean | no | Extract signature data from the finance document |

## Response

```json
{
  "success": true,
  "data": [
    {
      "docType": "string",
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
        "customerCity": {
          "confidence": 1,
          "page": 1,
          "value": "string"
        },
        "customerCountry": {
          "confidence": 1,
          "value": "string"
        },
        "customerName": {
          "confidence": 1,
          "page": 1,
          "value": "Ava Chen"
        },
        "customerStreet": {
          "confidence": 1,
          "page": 1,
          "value": "string"
        },
        "customerZip": {
          "confidence": 1,
          "page": 1,
          "value": "string"
        },
        "documentType": {
          "confidence": 1,
          "page": 1,
          "value": "string"
        },
        "email": {
          "confidence": 1,
          "page": 1,
          "value": "ava@example.com"
        },
        "invoiceDate": {
          "confidence": 1,
          "page": 1,
          "value": "2026-05-07T12:00:00.000Z"
        },
        "invoiceDueDate": {
          "confidence": 1,
          "page": 1,
          "value": "2026-05-07T12:00:00.000Z"
        },
        "invoiceNumber": {
          "confidence": 1,
          "page": 1,
          "value": "string"
        },
        "orderNumber": {
          "confidence": 1,
          "page": 1,
          "value": "string"
        },
        "reverseCharge": {
          "confidence": 1,
          "value": "string"
        },
        "shopCity": {
          "confidence": 1,
          "page": 1,
          "value": "string"
        },
        "shopCountry": {
          "confidence": 1,
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
        "shopZip": {
          "confidence": 1,
          "page": 1,
          "value": "string"
        },
        "taxAmount": {
          "confidence": 1,
          "value": "string"
        },
        "taxGrossAmount": {
          "confidence": 1,
          "page": 1,
          "value": "string"
        },
        "taxNetAmount": {
          "confidence": 1,
          "value": "string"
        },
        "taxPercentage": {
          "confidence": 1,
          "value": "string"
        },
        "totalPrice": {
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
      "paymentBanks": {},
      "payments": {},
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
          },
          "productQuantity": {
            "confidence": 1,
            "page": 1,
            "value": "string"
          },
          "productUnitPrice": {
            "confidence": 1,
            "page": 1,
            "value": "string"
          },
          "taxAmount": {
            "confidence": 1,
            "value": "string"
          },
          "taxGrossAmount": {
            "confidence": 1,
            "value": "string"
          },
          "taxNetAmount": {
            "confidence": 1,
            "page": 1,
            "value": "string"
          },
          "taxPercentage": {
            "confidence": 1,
            "value": "string"
          }
        }
      ],
      "qrCodes": {},
      "signatureImages": {},
      "signatures": {},
      "taxes": [
        {
          "taxAmount": {
            "confidence": 1,
            "page": 1,
            "value": "string"
          },
          "taxGrossAmount": {
            "confidence": 1,
            "page": 1,
            "value": "string"
          },
          "taxNetAmount": {
            "confidence": 1,
            "page": 1,
            "value": "string"
          },
          "taxPercentage": {
            "confidence": 1,
            "value": "string"
          }
        }
      ],
      "templateId": {},
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
| `docType` | string |  |
| `fileHash` | string |  |
| `fullText` | object |  |
| `general.category.confidence` | number |  |
| `general.category.value` | string |  |
| `general.currency.confidence` | number |  |
| `general.currency.value` | string |  |
| `general.customerCity.confidence` | number |  |
| `general.customerCity.page` | number |  |
| `general.customerCity.value` | string |  |
| `general.customerCountry.confidence` | number |  |
| `general.customerCountry.value` | string |  |
| `general.customerName.confidence` | number |  |
| `general.customerName.page` | number |  |
| `general.customerName.value` | string |  |
| `general.customerStreet.confidence` | number |  |
| `general.customerStreet.page` | number |  |
| `general.customerStreet.value` | string |  |
| `general.customerZip.confidence` | number |  |
| `general.customerZip.page` | number |  |
| `general.customerZip.value` | string |  |
| `general.documentType.confidence` | number |  |
| `general.documentType.page` | number |  |
| `general.documentType.value` | string |  |
| `general.email.confidence` | number |  |
| `general.email.page` | number |  |
| `general.email.value` | string |  |
| `general.invoiceDate.confidence` | number |  |
| `general.invoiceDate.page` | number |  |
| `general.invoiceDate.value` | date |  |
| `general.invoiceDueDate.confidence` | number |  |
| `general.invoiceDueDate.page` | number |  |
| `general.invoiceDueDate.value` | date |  |
| `general.invoiceNumber.confidence` | number |  |
| `general.invoiceNumber.page` | number |  |
| `general.invoiceNumber.value` | string |  |
| `general.orderNumber.confidence` | number |  |
| `general.orderNumber.page` | number |  |
| `general.orderNumber.value` | string |  |
| `general.reverseCharge.confidence` | number |  |
| `general.reverseCharge.value` | string |  |
| `general.shopCity.confidence` | number |  |
| `general.shopCity.page` | number |  |
| `general.shopCity.value` | string |  |
| `general.shopCountry.confidence` | number |  |
| `general.shopCountry.value` | string |  |
| `general.shopName.confidence` | number |  |
| `general.shopName.page` | number |  |
| `general.shopName.value` | string |  |
| `general.shopStreet.confidence` | number |  |
| `general.shopStreet.page` | number |  |
| `general.shopStreet.value` | string |  |
| `general.shopZip.confidence` | number |  |
| `general.shopZip.page` | number |  |
| `general.shopZip.value` | string |  |
| `general.taxAmount.confidence` | number |  |
| `general.taxAmount.value` | string |  |
| `general.taxGrossAmount.confidence` | number |  |
| `general.taxGrossAmount.page` | number |  |
| `general.taxGrossAmount.value` | string |  |
| `general.taxNetAmount.confidence` | number |  |
| `general.taxNetAmount.value` | string |  |
| `general.taxPercentage.confidence` | number |  |
| `general.taxPercentage.value` | string |  |
| `general.totalPrice.confidence` | number |  |
| `general.totalPrice.page` | number |  |
| `general.totalPrice.value` | string |  |
| `languages[]` | string |  |
| `mainLanguage` | string |  |
| `numberOfPages` | number |  |
| `pages[].height` | number |  |
| `pages[].width` | number |  |
| `paymentBanks` | object |  |
| `payments` | object |  |
| `performanceOption` | string |  |
| `productItems[].currency.confidence` | number |  |
| `productItems[].currency.value` | string |  |
| `productItems[].productName.confidence` | number |  |
| `productItems[].productName.page` | number |  |
| `productItems[].productName.value` | string |  |
| `productItems[].productPrice.confidence` | number |  |
| `productItems[].productPrice.page` | number |  |
| `productItems[].productPrice.value` | string |  |
| `productItems[].productQuantity.confidence` | number |  |
| `productItems[].productQuantity.page` | number |  |
| `productItems[].productQuantity.value` | string |  |
| `productItems[].productUnitPrice.confidence` | number |  |
| `productItems[].productUnitPrice.page` | number |  |
| `productItems[].productUnitPrice.value` | string |  |
| `productItems[].taxAmount.confidence` | number |  |
| `productItems[].taxAmount.value` | string |  |
| `productItems[].taxGrossAmount.confidence` | number |  |
| `productItems[].taxGrossAmount.value` | string |  |
| `productItems[].taxNetAmount.confidence` | number |  |
| `productItems[].taxNetAmount.page` | number |  |
| `productItems[].taxNetAmount.value` | string |  |
| `productItems[].taxPercentage.confidence` | number |  |
| `productItems[].taxPercentage.value` | string |  |
| `qrCodes` | object |  |
| `signatureImages` | object |  |
| `signatures` | object |  |
| `taxes[].taxAmount.confidence` | number |  |
| `taxes[].taxAmount.page` | number |  |
| `taxes[].taxAmount.value` | string |  |
| `taxes[].taxGrossAmount.confidence` | number |  |
| `taxes[].taxGrossAmount.page` | number |  |
| `taxes[].taxGrossAmount.value` | string |  |
| `taxes[].taxNetAmount.confidence` | number |  |
| `taxes[].taxNetAmount.page` | number |  |
| `taxes[].taxNetAmount.value` | string |  |
| `taxes[].taxPercentage.confidence` | number |  |
| `taxes[].taxPercentage.value` | string |  |
| `templateId` | object |  |
| `verification.nonDuplication.flagValid` | boolean |  |
| `verification.nonDuplication.message` | string |  |
| `verification.productsSumVsTotalPrice.flagValid` | boolean |  |
| `verification.productsSumVsTotalPrice.message` | string |  |
| `verification.taxPercentage.flagValid` | boolean |  |
| `verification.taxPercentage.message` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Eagle Doc API, this operation is `POST /api/finance/v1/processing` (base URL `https://de.eagle-doc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/process-finance-document.md) for the provider-specific parameters and requirements.

