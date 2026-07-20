# Moco: Get Offer



```
GET https://connect.mindcloud.co/v1/universal/moco/latest/actions/get-offer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moco `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moco/latest/actions/get-offer?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moco/latest/actions/get-offer?${params}`, {
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
| `id` | number | yes | Offer ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {
        "id": 1,
        "name": "Ava Chen"
      },
      "createdAt": "string",
      "createdOn": "string",
      "currency": "string",
      "customerApproval": {},
      "customProperties": {},
      "date": "string",
      "deal": {},
      "discount": 1,
      "dueDate": "string",
      "footer": "string",
      "grossTotal": 1,
      "id": 1,
      "identifier": "string",
      "internalContact": {
        "firstname": "Ava",
        "id": 1,
        "lastname": "Chen"
      },
      "invoiceId": {},
      "items": [
        [
          {}
        ]
      ],
      "netTotal": 1,
      "offerConfirmation": {},
      "project": {},
      "recipientAddress": "string",
      "salutation": "string",
      "status": "string",
      "tags": [
        [
          "string"
        ]
      ],
      "tax": 1,
      "title": "string",
      "updatedAt": "string",
      "updatedOn": "string",
      "user": {
        "firstname": "Ava",
        "id": 1,
        "lastname": "Chen"
      },
      "vat": {
        "active": true,
        "code": {},
        "creditAccount": {},
        "description": "string",
        "id": 1,
        "intraEu": true,
        "noticeTaxExemption": "string",
        "noticeTaxExemptionAlt": "string",
        "noticeTaxExemptionEn": "string",
        "printGrossTotal": true,
        "reverseCharge": true,
        "tax": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | object |  |
| `company.id` | number |  |
| `company.name` | string |  |
| `createdAt` | string |  |
| `createdOn` | string |  |
| `currency` | string |  |
| `customerApproval` | object |  |
| `customProperties` | object |  |
| `date` | string |  |
| `deal` | object |  |
| `discount` | number |  |
| `dueDate` | string |  |
| `footer` | string |  |
| `grossTotal` | number |  |
| `id` | number |  |
| `identifier` | string |  |
| `internalContact` | object |  |
| `internalContact.firstname` | string |  |
| `internalContact.id` | number |  |
| `internalContact.lastname` | string |  |
| `invoiceId` | object |  |
| `items[]` | array<object> |  |
| `items[].description` | object |  |
| `items[].id` | number |  |
| `items[].netTotal` | number |  |
| `items[].optional` | boolean |  |
| `items[].quantity` | number |  |
| `items[].revenueCategory` | object |  |
| `items[].serviceType` | string |  |
| `items[].title` | string |  |
| `items[].type` | string |  |
| `items[].unit` | string |  |
| `items[].unitCost` | object |  |
| `items[].unitPrice` | number |  |
| `netTotal` | number |  |
| `offerConfirmation` | object |  |
| `project` | object |  |
| `recipientAddress` | string |  |
| `salutation` | string |  |
| `status` | string |  |
| `tags[]` | array<string> |  |
| `tax` | number |  |
| `title` | string |  |
| `updatedAt` | string |  |
| `updatedOn` | string |  |
| `user` | object |  |
| `user.firstname` | string |  |
| `user.id` | number |  |
| `user.lastname` | string |  |
| `vat` | object |  |
| `vat.active` | boolean |  |
| `vat.code` | object |  |
| `vat.creditAccount` | object |  |
| `vat.description` | string |  |
| `vat.id` | number |  |
| `vat.intraEu` | boolean |  |
| `vat.noticeTaxExemption` | string |  |
| `vat.noticeTaxExemptionAlt` | string |  |
| `vat.noticeTaxExemptionEn` | string |  |
| `vat.printGrossTotal` | boolean |  |
| `vat.reverseCharge` | boolean |  |
| `vat.tax` | number |  |

## Native endpoint

Through the native Moco API, this operation is `GET /offers/:id` (base URL `https://{{credentials.domain}}.mocoapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-offer.md) for the provider-specific parameters and requirements.

