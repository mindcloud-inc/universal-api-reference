# Moco: List Purchases



```
GET https://connect.mindcloud.co/v1/universal/moco/latest/actions/list-purchases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moco `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moco/latest/actions/list-purchases?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moco/latest/actions/list-purchases?${params}`, {
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
| `categoryId` | number | no |  |
| `companyId` | number | no |  |
| `customProperties` | object | no |  |
| `date` | string | no |  |
| `identifier` | string | no |  |
| `ids` | string | no |  |
| `notBooked` | boolean | no |  |
| `paymentMethod` | string | no |  |
| `receiptIdentifier` | string | no |  |
| `status` | string | no |  |
| `tags` | string | no |  |
| `term` | string | no |  |
| `unpaid` | boolean | no |  |
| `updatedAfter` | date | no |  |

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

Through the native Moco API, this operation is `GET /purchases` (base URL `https://{{credentials.domain}}.mocoapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-purchases.md) for the provider-specific parameters and requirements.

