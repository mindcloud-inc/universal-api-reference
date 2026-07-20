# Simpro: Get Customer



```
GET https://connect.mindcloud.co/v1/universal/simpro/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simpro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpro/latest/actions/get-customer?connectionId=$CONNECTION_ID&companyId=0&customerId=3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "0",
  "customerId": "3"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpro/latest/actions/get-customer?${params}`, {
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
| `companyId` | number | yes | Simpro company ID. Single-company builds usually use 0. Default: `0`. Example: `0`. |
| `customerId` | number | yes | Company customer ID. Example: `3`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `columns[]` | array<string> | no | Specific customer fields to return. Example: `ID,CompanyName,Email`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "address": "string",
        "city": "string",
        "country": "string",
        "postalCode": "string",
        "state": "string"
      },
      "altPhone": "string",
      "amountOwing": 1,
      "archived": true,
      "banking": {
        "accountName": "Ava Chen",
        "accountNo": "string",
        "creditLimit": 1,
        "onStop": true,
        "paymentMethod": {},
        "paymentTermID": 1,
        "paymentTerms": {
          "days": 1,
          "type": "string"
        },
        "retention": "string",
        "routingNo": "string",
        "vendorOrderNoRequired": true
      },
      "billingAddress": {
        "address": "string",
        "city": "string",
        "country": "string",
        "postalCode": "string",
        "state": "string"
      },
      "companyName": "Ava Chen",
      "companyNumber": "string",
      "customerType": "string",
      "dateCreated": "string",
      "dateModified": "string",
      "doNotCall": true,
      "ein": "string",
      "email": "ava@example.com",
      "fax": "string",
      "id": 1,
      "phone": "string",
      "profile": {
        "accountManager": {},
        "currency": {
          "id": "string",
          "name": "Ava Chen",
          "visible": true
        },
        "customerGroup": {},
        "customerProfile": {},
        "notes": "string",
        "serviceJobCostCenter": {}
      },
      "rates": {
        "alwaysDeductCIS": true,
        "discountFee": 1,
        "labourTaxCode": {},
        "material": {
          "markup": 1,
          "pricingTier": {
            "defaultMarkup": 1,
            "id": 1,
            "name": "Ava Chen"
          }
        },
        "partTaxCode": {}
      },
      "sites": [
        {
          "id": 1,
          "name": "Ava Chen"
        }
      ],
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.address` | string |  |
| `address.city` | string |  |
| `address.country` | string |  |
| `address.postalCode` | string |  |
| `address.state` | string |  |
| `altPhone` | string |  |
| `amountOwing` | number |  |
| `archived` | boolean |  |
| `banking.accountName` | string |  |
| `banking.accountNo` | string |  |
| `banking.creditLimit` | number |  |
| `banking.onStop` | boolean |  |
| `banking.paymentMethod` | object |  |
| `banking.paymentTermID` | number |  |
| `banking.paymentTerms.days` | number |  |
| `banking.paymentTerms.type` | string |  |
| `banking.retention` | string |  |
| `banking.routingNo` | string |  |
| `banking.vendorOrderNoRequired` | boolean |  |
| `billingAddress.address` | string |  |
| `billingAddress.city` | string |  |
| `billingAddress.country` | string |  |
| `billingAddress.postalCode` | string |  |
| `billingAddress.state` | string |  |
| `companyName` | string |  |
| `companyNumber` | string |  |
| `customerType` | string |  |
| `dateCreated` | string |  |
| `dateModified` | string |  |
| `doNotCall` | boolean |  |
| `ein` | string |  |
| `email` | string |  |
| `fax` | string |  |
| `id` | number |  |
| `phone` | string |  |
| `profile.accountManager` | object |  |
| `profile.currency.id` | string |  |
| `profile.currency.name` | string |  |
| `profile.currency.visible` | boolean |  |
| `profile.customerGroup` | object |  |
| `profile.customerProfile` | object |  |
| `profile.notes` | string |  |
| `profile.serviceJobCostCenter` | object |  |
| `rates.alwaysDeductCIS` | boolean |  |
| `rates.discountFee` | number |  |
| `rates.labourTaxCode` | object |  |
| `rates.material.markup` | number |  |
| `rates.material.pricingTier.defaultMarkup` | number |  |
| `rates.material.pricingTier.id` | number |  |
| `rates.material.pricingTier.name` | string |  |
| `rates.partTaxCode` | object |  |
| `sites[].id` | number |  |
| `sites[].name` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Simpro API, this operation is `GET /companies/:companyId/customers/companies/:customerId` (base URL `https://mindcloud.simprosuite.com/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

