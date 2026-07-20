# Moco: Create Purchase



```
POST https://connect.mindcloud.co/v1/universal/moco/latest/actions/create-purchase
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moco `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moco/latest/actions/create-purchase" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moco/latest/actions/create-purchase', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | string | no |  |
| `currency` | string | no |  |
| `customPropertyValues` | string | no |  |
| `date` | string | no |  |
| `dueDate` | string | no |  |
| `file` | string | no |  |
| `iban` | string | no |  |
| `info` | string | no |  |
| `items[]` | array<object> | no |  |
| `paymentMethod` | string | no |  |
| `receiptIdentifier` | string | no |  |
| `reference` | string | no |  |
| `servicePeriodFrom` | string | no |  |
| `servicePeriodTo` | string | no |  |
| `status` | string | no |  |
| `tags` | string | no |  |
| `title` | string | no |  |
| `userId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approvalStatus": "string",
      "company": {},
      "createdAt": "string",
      "creditCardTransaction": {},
      "currency": "string",
      "customProperties": {},
      "date": "string",
      "dueDate": {},
      "fileUrl": {},
      "grossTotal": 1,
      "iban": {},
      "id": 1,
      "identifier": "string",
      "info": {},
      "items": [
        [
          {}
        ]
      ],
      "netTotal": 1,
      "paymentMethod": "string",
      "payments": [
        [
          "string"
        ]
      ],
      "receiptIdentifier": {},
      "reference": {},
      "refundRequest": {},
      "servicePeriodFrom": {},
      "servicePeriodTo": {},
      "status": "string",
      "tags": [
        [
          "string"
        ]
      ],
      "title": "string",
      "updatedAt": "string",
      "user": {
        "firstname": "Ava",
        "id": 1,
        "lastname": "Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approvalStatus` | string |  |
| `company` | object |  |
| `createdAt` | string |  |
| `creditCardTransaction` | object |  |
| `currency` | string |  |
| `customProperties` | object |  |
| `date` | string |  |
| `dueDate` | object |  |
| `fileUrl` | object |  |
| `grossTotal` | number |  |
| `iban` | object |  |
| `id` | number |  |
| `identifier` | string |  |
| `info` | object |  |
| `items[]` | array<object> |  |
| `items[].category` | object |  |
| `items[].expense` | object |  |
| `items[].grossTotal` | number |  |
| `items[].id` | number |  |
| `items[].netTotal` | number |  |
| `items[].receipt` | object |  |
| `items[].supplierCreditNumber` | number |  |
| `items[].tax` | number |  |
| `items[].taxIncluded` | boolean |  |
| `items[].taxTotal` | number |  |
| `items[].title` | string |  |
| `items[].vat` | object |  |
| `items[].vat.active` | boolean |  |
| `items[].vat.code` | object |  |
| `items[].vat.description` | string |  |
| `items[].vat.id` | number |  |
| `items[].vat.intraEu` | boolean |  |
| `items[].vat.reverseCharge` | boolean |  |
| `items[].vat.tax` | number |  |
| `netTotal` | number |  |
| `paymentMethod` | string |  |
| `payments[]` | array<string> |  |
| `receiptIdentifier` | object |  |
| `reference` | object |  |
| `refundRequest` | object |  |
| `servicePeriodFrom` | object |  |
| `servicePeriodTo` | object |  |
| `status` | string |  |
| `tags[]` | array<string> |  |
| `title` | string |  |
| `updatedAt` | string |  |
| `user` | object |  |
| `user.firstname` | string |  |
| `user.id` | number |  |
| `user.lastname` | string |  |

## Native endpoint

Through the native Moco API, this operation is `POST /purchases` (base URL `https://{{credentials.domain}}.mocoapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-purchase.md) for the provider-specific parameters and requirements.

