# Moco: Create Invoice



```
POST https://connect.mindcloud.co/v1/universal/moco/latest/actions/create-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moco `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moco/latest/actions/create-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moco/latest/actions/create-invoice', {
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
| `cashDiscount` | string | no |  |
| `cashDiscountDays` | string | no |  |
| `changeAddress` | string | no |  |
| `currency` | string | no |  |
| `customerId` | string | no |  |
| `customProperties` | string | no |  |
| `date` | string | no |  |
| `discount` | string | no |  |
| `dueDate` | string | no |  |
| `footer` | string | no |  |
| `internalContactId` | string | no |  |
| `items[]` | array<object> | no |  |
| `printDetailColumns` | string | no |  |
| `projectId` | string | no |  |
| `recipientAddress` | string | no |  |
| `salutation` | string | no |  |
| `servicePeriodFrom` | string | no |  |
| `servicePeriodTo` | string | no |  |
| `status` | string | no |  |
| `tags` | string | no |  |
| `tax` | string | no |  |
| `title` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activityHoursModified": true,
      "cashDiscount": 1,
      "cashDiscountDays": 1,
      "createdAt": "string",
      "createdOn": "string",
      "creditNumber": {},
      "creditorReference": {},
      "currency": "string",
      "customerId": 1,
      "customProperties": {},
      "date": "string",
      "debitNumber": {},
      "discount": 1,
      "dueDate": "string",
      "fileUrl": {},
      "footer": "string",
      "grossTotal": 1,
      "id": 1,
      "identifier": "string",
      "internalContact": {
        "firstname": "Ava",
        "id": 1,
        "lastname": "Chen"
      },
      "items": [
        [
          {}
        ]
      ],
      "locked": true,
      "netTotal": 1,
      "offerId": {},
      "payments": [
        [
          "string"
        ]
      ],
      "projectId": {},
      "recipientAddress": "string",
      "reminders": [
        [
          "string"
        ]
      ],
      "reversal": true,
      "reversalInvoiceId": {},
      "reversed": true,
      "reversedInvoiceId": {},
      "salutation": "string",
      "servicePeriod": "string",
      "servicePeriodFrom": {},
      "servicePeriodTo": {},
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
| `activityHoursModified` | boolean |  |
| `cashDiscount` | number |  |
| `cashDiscountDays` | number |  |
| `createdAt` | string |  |
| `createdOn` | string |  |
| `creditNumber` | object |  |
| `creditorReference` | object |  |
| `currency` | string |  |
| `customerId` | number |  |
| `customProperties` | object |  |
| `date` | string |  |
| `debitNumber` | object |  |
| `discount` | number |  |
| `dueDate` | string |  |
| `fileUrl` | object |  |
| `footer` | string |  |
| `grossTotal` | number |  |
| `id` | number |  |
| `identifier` | string |  |
| `internalContact` | object |  |
| `internalContact.firstname` | string |  |
| `internalContact.id` | number |  |
| `internalContact.lastname` | string |  |
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
| `items[].unitPrice` | number |  |
| `locked` | boolean |  |
| `netTotal` | number |  |
| `offerId` | object |  |
| `payments[]` | array<string> |  |
| `projectId` | object |  |
| `recipientAddress` | string |  |
| `reminders[]` | array<string> |  |
| `reversal` | boolean |  |
| `reversalInvoiceId` | object |  |
| `reversed` | boolean |  |
| `reversedInvoiceId` | object |  |
| `salutation` | string |  |
| `servicePeriod` | string |  |
| `servicePeriodFrom` | object |  |
| `servicePeriodTo` | object |  |
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

Through the native Moco API, this operation is `POST /invoices` (base URL `https://{{credentials.domain}}.mocoapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice.md) for the provider-specific parameters and requirements.

