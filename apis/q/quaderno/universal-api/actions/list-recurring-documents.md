# Quaderno: List Recurring Documents

Retrieves recurring billing documents from Quaderno.

```
GET https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/list-recurring-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quaderno `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/list-recurring-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/list-recurring-documents?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `q` | string | no | Search text to filter recurring documents. Example: `Stage 3 recurring`. |
| `date` | date | no | Date filter for recurring documents. Example: `2026-03-20`. |
| `state` | string | no | State selector for recurring documents. Example: `active`. |
| `contact` | number | no | Contact ID selector for recurring documents. Example: `9289221`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": {
        "contactPerson": {},
        "createdAt": 1,
        "department": {},
        "email": "ava@example.com",
        "fullName": "Ava Chen",
        "id": 1,
        "kind": "string",
        "language": "string",
        "notes": "string",
        "permalink": "https://example.com",
        "phone1": {},
        "processor": {},
        "processorId": {},
        "taxId": {},
        "taxStatus": "string",
        "web": {}
      },
      "currency": "string",
      "customMetadata": {
        "source": "string"
      },
      "discount": 1,
      "dueDays": 1,
      "endDate": {},
      "frequency": "string",
      "id": 1,
      "items": [
        {
          "description": "string",
          "discountCents": 1,
          "discountRate": 1,
          "grossAmountCents": "string",
          "id": 1,
          "productCode": {},
          "quantity": 1,
          "reference": {},
          "subtotalCents": 1,
          "tax1Country": {},
          "tax1Name": {},
          "tax1Rate": {},
          "tax1Region": {},
          "tax1TransactionType": "string",
          "tax2Country": {},
          "tax2Name": {},
          "tax2Rate": {},
          "tax2Region": {},
          "tax2TransactionType": "string",
          "unitPriceCents": 1
        }
      ],
      "notes": "string",
      "paymentDetails": {},
      "poNumber": {},
      "recurringDocument": "string",
      "recurringFrequency": 1,
      "recurringPeriod": "string",
      "startDate": "string",
      "state": "string",
      "subject": "string",
      "subtotal": 1,
      "totalCents": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact.contactPerson` | object |  |
| `contact.createdAt` | number |  |
| `contact.department` | object |  |
| `contact.email` | string |  |
| `contact.fullName` | string |  |
| `contact.id` | number |  |
| `contact.kind` | string |  |
| `contact.language` | string |  |
| `contact.notes` | string |  |
| `contact.permalink` | string |  |
| `contact.phone1` | object |  |
| `contact.processor` | object |  |
| `contact.processorId` | object |  |
| `contact.taxId` | object |  |
| `contact.taxStatus` | string |  |
| `contact.web` | object |  |
| `currency` | string |  |
| `customMetadata.source` | string |  |
| `discount` | number |  |
| `dueDays` | number |  |
| `endDate` | object |  |
| `frequency` | string |  |
| `id` | number |  |
| `items[].description` | string |  |
| `items[].discountCents` | number |  |
| `items[].discountRate` | number |  |
| `items[].grossAmountCents` | string |  |
| `items[].id` | number |  |
| `items[].productCode` | object |  |
| `items[].quantity` | number |  |
| `items[].reference` | object |  |
| `items[].subtotalCents` | number |  |
| `items[].tax1Country` | object |  |
| `items[].tax1Name` | object |  |
| `items[].tax1Rate` | object |  |
| `items[].tax1Region` | object |  |
| `items[].tax1TransactionType` | string |  |
| `items[].tax2Country` | object |  |
| `items[].tax2Name` | object |  |
| `items[].tax2Rate` | object |  |
| `items[].tax2Region` | object |  |
| `items[].tax2TransactionType` | string |  |
| `items[].unitPriceCents` | number |  |
| `notes` | string |  |
| `paymentDetails` | object |  |
| `poNumber` | object |  |
| `recurringDocument` | string |  |
| `recurringFrequency` | number |  |
| `recurringPeriod` | string |  |
| `startDate` | string |  |
| `state` | string |  |
| `subject` | string |  |
| `subtotal` | number |  |
| `totalCents` | number |  |
| `url` | string |  |

## Native endpoint

Through the native Quaderno API, this operation is `GET /recurring` (base URL `https://sandbox-quadernoapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recurring-documents.md) for the provider-specific parameters and requirements.

