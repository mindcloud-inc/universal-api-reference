# Zahara: Update Supplier

Updates an existing supplier in Zahara.

```
PUT https://connect.mindcloud.co/v1/universal/zahara/latest/actions/update-supplier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zahara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zahara/latest/actions/update-supplier" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "supplierId": "729006",
  "address": {},
  "businessUnitId": 1,
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
  "referenceNumber": "string",
  "supplierName": "Ava Chen",
  "void": true,
  "isActive": true,
  "defaultCostCode": "string",
  "defaultCurrencyId": 1,
  "trustedStatus": true,
  "supplierRecordId": 1,
  "defaultNominalCodeId": 1,
  "defaultTaxCodeId": 1,
  "defaultCostCodeId": 1,
  "lastUpdated": "string",
  "dateCreated": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zahara/latest/actions/update-supplier', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "supplierId": "729006",
    "address": {},
    "businessUnitId": 1,
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
    "referenceNumber": "string",
    "supplierName": "Ava Chen",
    "void": true,
    "isActive": true,
    "defaultCostCode": "string",
    "defaultCurrencyId": 1,
    "trustedStatus": true,
    "supplierRecordId": 1,
    "defaultNominalCodeId": 1,
    "defaultTaxCodeId": 1,
    "defaultCostCodeId": 1,
    "lastUpdated": "string",
    "dateCreated": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `supplierId` | number | yes | The Zahara supplier ID to update. Example: `729006`. |
| `address` | object | yes | Supplier address object. |
| `businessUnitId` | number | yes | Business unit ID. |
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
| `referenceNumber` | string | yes | Supplier reference number. |
| `supplierName` | string | yes | Supplier display name. |
| `void` | boolean | yes | Whether the supplier is void. |
| `isActive` | boolean | yes | Whether the supplier is active. |
| `defaultCostCode` | string | yes | Default cost code. |
| `defaultCurrencyId` | number | yes | Default currency ID. |
| `trustedStatus` | boolean | yes | Trusted supplier status. |
| `bankAccountNumber` | string | no | Supplier bank account number. |
| `supplierRecordId` | number | yes | Supplier ID echoed in the update body. |
| `bankSortCode` | string | no | Supplier bank sort code. |
| `defaultNominalCodeId` | number | yes | Default nominal code ID. |
| `defaultTaxCodeId` | number | yes | Default tax code ID. |
| `defaultCostCodeId` | number | yes | Default cost code ID. |
| `lastUpdated` | string | yes | Supplier last-updated timestamp. |
| `dateCreated` | string | yes | Supplier created timestamp. |

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
| `SupplierId` | number | Supplier ID represented for successful update operations in MindCloud. |

## Native endpoint

Through the native Zahara API, this operation is `PUT /api/{{credentials.businessUnitApiKey}}/Supplier/Update/{{supplierId}}` (base URL `https://api.myzahara.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-supplier.md) for the provider-specific parameters and requirements.

