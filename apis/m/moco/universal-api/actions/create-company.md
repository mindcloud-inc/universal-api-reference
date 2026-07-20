# Moco: Create Company



```
POST https://connect.mindcloud.co/v1/universal/moco/latest/actions/create-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moco `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moco/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moco/latest/actions/create-company', {
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
| `address` | string | no |  |
| `alternativeCorrespondenceLanguage` | string | no |  |
| `bankBic` | string | no |  |
| `bankOwner` | string | no |  |
| `billingEmailCc` | string | no |  |
| `billingNotes` | string | no |  |
| `countryCode` | string | no |  |
| `creditNumber` | string | no |  |
| `currency` | string | no |  |
| `customerTax` | string | no |  |
| `customerVatCodeId` | string | no |  |
| `customProperties` | string | no |  |
| `debitNumber` | string | no |  |
| `defaultInvoiceDueDays` | string | no |  |
| `defaultPaymentMeans` | string | no |  |
| `email` | string | no |  |
| `fax` | string | no |  |
| `footer` | string | no |  |
| `iban` | string | no |  |
| `identifier` | string | no |  |
| `info` | string | no |  |
| `invoiceFormat` | string | no |  |
| `name` | string | no |  |
| `phone` | string | no |  |
| `supplierTax` | string | no |  |
| `supplierVatCodeId` | string | no |  |
| `tags` | string | no |  |
| `type` | string | no |  |
| `userId` | string | no |  |
| `vatIdentifier` | string | no |  |
| `website` | string | no |  |

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
          "string"
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
| `projects[]` | array<string> |  |
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

Through the native Moco API, this operation is `POST /companies` (base URL `https://{{credentials.domain}}.mocoapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company.md) for the provider-specific parameters and requirements.

