# Zahara: Create Supplier

Creates a new supplier in Zahara.

```
POST https://connect.mindcloud.co/v1/universal/zahara/latest/actions/create-supplier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zahara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zahara/latest/actions/create-supplier" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "address": {},
  "contactName": "Ava Chen",
  "countryCode": "string",
  "countryCodeId": 1,
  "defaultNominalCode": "string",
  "defaultPaymentTerms": 1,
  "paymentTermStartType": 1,
  "paymentTermDaysNumber": 1,
  "paymentTermType": 1,
  "defaultTaxCode": "string",
  "email": "ava@example.com",
  "supplierEmails[]": [
    {}
  ],
  "referenceNumber": "string",
  "supplierName": "Ava Chen",
  "void": true,
  "isActive": true,
  "defaultCostCode": "string",
  "defaultCurrencyId": 1,
  "trustedStatus": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zahara/latest/actions/create-supplier', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "address": {},
    "contactName": "Ava Chen",
    "countryCode": "string",
    "countryCodeId": 1,
    "defaultNominalCode": "string",
    "defaultPaymentTerms": 1,
    "paymentTermStartType": 1,
    "paymentTermDaysNumber": 1,
    "paymentTermType": 1,
    "defaultTaxCode": "string",
    "email": "ava@example.com",
    "supplierEmails[]": [{}],
    "referenceNumber": "string",
    "supplierName": "Ava Chen",
    "void": true,
    "isActive": true,
    "defaultCostCode": "string",
    "defaultCurrencyId": 1,
    "trustedStatus": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | object | yes | Supplier address object. |
| `contactName` | string | yes | Primary supplier contact name. |
| `countryCode` | string | yes | Supplier ISO country code. |
| `countryCodeId` | number | yes | Supplier country code ID. |
| `defaultNominalCode` | string | yes | Default nominal code. |
| `defaultPaymentTerms` | number | yes | Default payment terms value. |
| `paymentTermStartType` | number | yes | Payment term start type. |
| `paymentTermDaysNumber` | number | yes | Payment term days number. |
| `paymentTermType` | number | yes | Payment term type. |
| `defaultTaxCode` | string | yes | Default tax code. |
| `email` | string | yes | Primary supplier email. |
| `supplierEmails[]` | array<object> | yes | Supplier email list. |
| `referenceNumber` | string | yes | Supplier reference number. |
| `supplierName` | string | yes | Supplier display name. |
| `void` | boolean | yes | Whether the supplier is void. |
| `isActive` | boolean | yes | Whether the supplier is active. |
| `defaultCostCode` | string | yes | Default cost code. |
| `defaultCurrencyId` | number | yes | Default currency ID. |
| `trustedStatus` | boolean | yes | Trusted supplier status. |
| `bankAccountNumber` | string | no | Supplier bank account number. |
| `bankSortCode` | string | no | Supplier bank sort code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "SupplierId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `SupplierId` | number | Created supplier ID returned by Zahara. |

## Native endpoint

Through the native Zahara API, this operation is `POST /api/{{credentials.businessUnitApiKey}}/Supplier/Add` (base URL `https://api.myzahara.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-supplier.md) for the provider-specific parameters and requirements.

