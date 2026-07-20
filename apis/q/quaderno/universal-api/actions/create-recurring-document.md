# Quaderno: Create Recurring Document

Creates a recurring billing document in Quaderno.

```
POST https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/create-recurring-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quaderno `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/create-recurring-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contact.first_name": "Stage3",
  "items[].description": "Monthly advisory service",
  "items[].unit_price": "49.99"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/create-recurring-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contact.first_name": "Stage3",
    "items[].description": "Monthly advisory service",
    "items[].unit_price": "49.99"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `startDate` | date | no | Issue date for the first recurring document. Example: `2026-03-19`. |
| `endDate` | date | no | Issue date for the last recurring document. Example: `2026-12-31`. |
| `recurringPeriod` | string | no | Recurring period unit. Example: `months`. |
| `recurringFrequency` | number | no | Number of recurring periods between documents. Example: `1`. |
| `dueDays` | string | no | Number of days until payment is due. Example: `7`. |
| `currency` | string | no | Three-letter ISO currency code. Example: `USD`. |
| `paymentDetails` | string | no | Accepted payment method details. Example: `Charge card on file`. |
| `notes` | string | no | Extra notes for the recurring document. Example: `Created by MindCloud Stage 3`. |
| `contact.first_name` | string | yes | Contact first name. Example: `Stage3`. |
| `contact.last_name` | string | no | Contact last name. Example: `Tester`. |
| `contact.email` | string | no | Contact email address. Example: `apps+quaderno-recurring@mindcloud.co`. |
| `contact.country` | string | no | Two-letter ISO country code for the contact. Example: `US`. |
| `subject` | string | no | Summary description for the recurring document. Example: `Stage 3 recurring document`. |
| `items[].description` | string | yes | Line item description. Example: `Monthly advisory service`. |
| `items[].quantity` | number | no | Line item quantity. Example: `1`. |
| `items[].unit_price` | number | yes | Line item unit price. Example: `49.99`. |
| `items[].tax_1_transaction_type` | string | no | Primary tax classification for the line item. Example: `standard`. |
| `customMetadata` | object | no | Custom metadata object for the recurring document. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `frequency` | string | no | Deprecated recurring frequency option. Example: `monthly`. |

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

Through the native Quaderno API, this operation is `POST /recurring` (base URL `https://sandbox-quadernoapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-recurring-document.md) for the provider-specific parameters and requirements.

