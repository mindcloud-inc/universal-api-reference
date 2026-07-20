# Moco: Get Company



```
GET https://connect.mindcloud.co/v1/universal/moco/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moco `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moco/latest/actions/get-company?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moco/latest/actions/get-company?${params}`, {
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
| `id` | number | yes | Company ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "address": "string",
      "alternativeCorrespondenceLanguage": true,
      "archivedOn": {},
      "billingEmailCc": "ava@example.com",
      "billingNotes": "string",
      "billingTax": 1,
      "billingVat": {
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
      },
      "countryCode": "string",
      "createdAt": "string",
      "currency": "string",
      "customerVat": {
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
      },
      "customProperties": {},
      "customRates": true,
      "defaultCashDiscount": 1,
      "defaultCashDiscountDays": 1,
      "defaultDiscount": 1,
      "defaultInvoiceDueDays": 1,
      "defaultPaymentMeans": {},
      "email": {},
      "englishCorrespondenceLanguage": true,
      "fax": "string",
      "footer": "string",
      "id": 1,
      "identifier": "string",
      "includeTimeReport": true,
      "info": "string",
      "intern": true,
      "invoiceFormat": "string",
      "labels": [
        [
          "string"
        ]
      ],
      "name": "Ava Chen",
      "phone": "string",
      "projects": [
        [
          {}
        ]
      ],
      "tags": [
        [
          "string"
        ]
      ],
      "type": "string",
      "updatedAt": "string",
      "user": {
        "firstname": "Ava",
        "id": 1,
        "lastname": "Chen"
      },
      "vatIdentifier": {},
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `address` | string |  |
| `alternativeCorrespondenceLanguage` | boolean |  |
| `archivedOn` | object |  |
| `billingEmailCc` | string |  |
| `billingNotes` | string |  |
| `billingTax` | number |  |
| `billingVat` | object |  |
| `billingVat.active` | boolean |  |
| `billingVat.code` | object |  |
| `billingVat.creditAccount` | object |  |
| `billingVat.description` | string |  |
| `billingVat.id` | number |  |
| `billingVat.intraEu` | boolean |  |
| `billingVat.noticeTaxExemption` | string |  |
| `billingVat.noticeTaxExemptionAlt` | string |  |
| `billingVat.noticeTaxExemptionEn` | string |  |
| `billingVat.printGrossTotal` | boolean |  |
| `billingVat.reverseCharge` | boolean |  |
| `billingVat.tax` | number |  |
| `countryCode` | string |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `customerVat` | object |  |
| `customerVat.active` | boolean |  |
| `customerVat.code` | object |  |
| `customerVat.creditAccount` | object |  |
| `customerVat.description` | string |  |
| `customerVat.id` | number |  |
| `customerVat.intraEu` | boolean |  |
| `customerVat.noticeTaxExemption` | string |  |
| `customerVat.noticeTaxExemptionAlt` | string |  |
| `customerVat.noticeTaxExemptionEn` | string |  |
| `customerVat.printGrossTotal` | boolean |  |
| `customerVat.reverseCharge` | boolean |  |
| `customerVat.tax` | number |  |
| `customProperties` | object |  |
| `customRates` | boolean |  |
| `defaultCashDiscount` | number |  |
| `defaultCashDiscountDays` | number |  |
| `defaultDiscount` | number |  |
| `defaultInvoiceDueDays` | number |  |
| `defaultPaymentMeans` | object |  |
| `email` | object |  |
| `englishCorrespondenceLanguage` | boolean |  |
| `fax` | string |  |
| `footer` | string |  |
| `id` | number |  |
| `identifier` | string |  |
| `includeTimeReport` | boolean |  |
| `info` | string |  |
| `intern` | boolean |  |
| `invoiceFormat` | string |  |
| `labels[]` | array<string> |  |
| `name` | string |  |
| `phone` | string |  |
| `projects[]` | array<object> |  |
| `projects[].active` | boolean |  |
| `projects[].billable` | boolean |  |
| `projects[].id` | number |  |
| `projects[].identifier` | string |  |
| `projects[].name` | string |  |
| `tags[]` | array<string> |  |
| `type` | string |  |
| `updatedAt` | string |  |
| `user` | object |  |
| `user.firstname` | string |  |
| `user.id` | number |  |
| `user.lastname` | string |  |
| `vatIdentifier` | object |  |
| `website` | string |  |

## Native endpoint

Through the native Moco API, this operation is `GET /companies/:id` (base URL `https://{{credentials.domain}}.mocoapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

