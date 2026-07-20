# Moco: List Invoices



```
GET https://connect.mindcloud.co/v1/universal/moco/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moco `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moco/latest/actions/list-invoices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moco/latest/actions/list-invoices?${params}`, {
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
| `companyId` | number | no |  |
| `customProperties` | object | no |  |
| `dateFrom` | date | no |  |
| `dateTo` | date | no |  |
| `identifier` | string | no |  |
| `ids` | string | no |  |
| `includeDisregarded` | boolean | no |  |
| `notBooked` | boolean | no |  |
| `projectId` | number | no |  |
| `servicePeriodFrom` | date | no |  |
| `servicePeriodTo` | date | no |  |
| `status` | string | no |  |
| `tags` | string | no |  |
| `term` | string | no |  |
| `updatedAfter` | date | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
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
      "fileUrl": "https://example.com",
      "grossTotal": 1,
      "id": 1,
      "identifier": {},
      "locked": true,
      "netTotal": 1,
      "offerId": {},
      "projectId": {},
      "recipientAddress": "string",
      "reversal": true,
      "reversalInvoiceId": {},
      "reversed": true,
      "reversedInvoiceId": {},
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
| `fileUrl` | string |  |
| `grossTotal` | number |  |
| `id` | number |  |
| `identifier` | object |  |
| `locked` | boolean |  |
| `netTotal` | number |  |
| `offerId` | object |  |
| `projectId` | object |  |
| `recipientAddress` | string |  |
| `reversal` | boolean |  |
| `reversalInvoiceId` | object |  |
| `reversed` | boolean |  |
| `reversedInvoiceId` | object |  |
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

Through the native Moco API, this operation is `GET /invoices` (base URL `https://{{credentials.domain}}.mocoapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

