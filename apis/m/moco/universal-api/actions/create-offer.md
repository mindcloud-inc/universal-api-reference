# Moco: Create Offer



```
POST https://connect.mindcloud.co/v1/universal/moco/latest/actions/create-offer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moco `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moco/latest/actions/create-offer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moco/latest/actions/create-offer', {
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
| `changeAddress` | string | no |  |
| `companyId` | string | no |  |
| `contactId` | string | no |  |
| `currency` | string | no |  |
| `customProperties` | string | no |  |
| `date` | string | no |  |
| `dealId` | string | no |  |
| `discount` | string | no |  |
| `dueDate` | string | no |  |
| `footer` | string | no |  |
| `internalContactId` | string | no |  |
| `items[]` | array<object> | no |  |
| `printDetailColumns` | string | no |  |
| `projectId` | string | no |  |
| `recipientAddress` | string | no |  |
| `salutation` | string | no |  |
| `tags` | string | no |  |
| `tax` | string | no |  |
| `title` | string | no |  |

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
          "string"
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
| `items[]` | array<string> |  |
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

Through the native Moco API, this operation is `POST /offers` (base URL `https://{{credentials.domain}}.mocoapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-offer.md) for the provider-specific parameters and requirements.

