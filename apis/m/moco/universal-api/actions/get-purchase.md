# Moco: Get Purchase



```
GET https://connect.mindcloud.co/v1/universal/moco/latest/actions/get-purchase
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moco `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moco/latest/actions/get-purchase?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moco/latest/actions/get-purchase?${params}`, {
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
| `id` | number | yes | Purchase ID |

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

Through the native Moco API, this operation is `GET /purchases/:id` (base URL `https://{{credentials.domain}}.mocoapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-purchase.md) for the provider-specific parameters and requirements.

