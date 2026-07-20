# Quaderno: Create Receipt

Creates a paid receipt in Quaderno.

```
POST https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/create-receipt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quaderno `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/create-receipt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contact": {},
  "items[]": [
    {}
  ],
  "payments[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/create-receipt', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contact": {},
    "items[]": [{}],
    "payments[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contact` | object | yes | Existing contact object. |
| `currency` | string | no | Receipt currency code. |
| `items[]` | array<object> | yes | Receipt line items array. |
| `payments[]` | array<object> | yes | Receipt payments array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blocked": true,
      "city": "string",
      "contact": {
        "createdAt": 1,
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
      "country": "string",
      "createdAt": 1,
      "currency": "string",
      "deliveryState": {},
      "discountCents": 1,
      "id": 1,
      "issueDate": "string",
      "items": [
        {
          "description": "string",
          "discountCents": 1,
          "discountRate": 1,
          "grossAmountCents": 1,
          "id": 1,
          "productCode": "string",
          "quantity": 1,
          "reference": "string",
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
      "notes": {},
      "number": "string",
      "pdf": "string",
      "permalink": "https://example.com",
      "poNumber": {},
      "postalCode": "string",
      "processor": {},
      "processorFeeCents": {},
      "processorId": {},
      "region": "string",
      "secureId": "string",
      "state": "string",
      "streetLine1": "string",
      "streetLine2": {},
      "subject": {},
      "subtotalCents": 1,
      "taxId": {},
      "totalCents": 1,
      "url": "https://example.com",
      "verificationCode": {},
      "verificationPermalink": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blocked` | boolean |  |
| `city` | string |  |
| `contact.createdAt` | number |  |
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
| `country` | string |  |
| `createdAt` | number |  |
| `currency` | string |  |
| `deliveryState` | object |  |
| `discountCents` | number |  |
| `id` | number |  |
| `issueDate` | string |  |
| `items[].description` | string |  |
| `items[].discountCents` | number |  |
| `items[].discountRate` | number |  |
| `items[].grossAmountCents` | number |  |
| `items[].id` | number |  |
| `items[].productCode` | string |  |
| `items[].quantity` | number |  |
| `items[].reference` | string |  |
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
| `notes` | object |  |
| `number` | string |  |
| `pdf` | string |  |
| `permalink` | string |  |
| `poNumber` | object |  |
| `postalCode` | string |  |
| `processor` | object |  |
| `processorFeeCents` | object |  |
| `processorId` | object |  |
| `region` | string |  |
| `secureId` | string |  |
| `state` | string |  |
| `streetLine1` | string |  |
| `streetLine2` | object |  |
| `subject` | object |  |
| `subtotalCents` | number |  |
| `taxId` | object |  |
| `totalCents` | number |  |
| `url` | string |  |
| `verificationCode` | object |  |
| `verificationPermalink` | object |  |

## Native endpoint

Through the native Quaderno API, this operation is `POST /receipts` (base URL `https://sandbox-quadernoapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-receipt.md) for the provider-specific parameters and requirements.

