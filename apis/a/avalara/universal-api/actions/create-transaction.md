# Avalara AvaTax: Create Transaction



```
POST https://connect.mindcloud.co/v1/universal/avalara/latest/actions/create-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avalara AvaTax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/avalara/latest/actions/create-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "lines[]": [
    "string"
  ],
  "lines[].amount": 1,
  "customerCode": "string",
  "date": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avalara/latest/actions/create-transaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "lines[]": ["string"],
    "lines[].amount": 1,
    "customerCode": "string",
    "date": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `addresses.pointOfOrderOrigin.line1` | string | no |  |
| `addresses.shipFrom` | object | no |  |
| `addresses.shipFrom.line1` | string | no |  |
| `addresses.shipTo.line1` | string | no |  |
| `lines[]` | array | yes |  |
| `lines[].number` | string | no |  |
| `addresses.pointOfOrderOrigin.city` | string | no |  |
| `addresses.shipFrom.city` | string | no |  |
| `addresses.shipTo` | object | no |  |
| `addresses.shipTo.city` | string | no |  |
| `lines[].quantity` | number | no |  |
| `addresses.pointOfOrderOrigin` | object | no |  |
| `addresses.pointOfOrderOrigin.region` | string | no |  |
| `addresses.shipFrom.region` | string | no |  |
| `addresses.shipTo.region` | string | no |  |
| `lines[].amount` | number | yes |  |
| `addresses.pointOfOrderOrigin.country` | string | no |  |
| `addresses.shipFrom.country` | string | no |  |
| `addresses.shipTo.country` | string | no |  |
| `lines[].taxCode` | string | no |  |
| `addresses.pointOfOrderOrigin.postalCode` | string | no |  |
| `addresses.shipFrom.postalCode` | string | no |  |
| `addresses.shipTo.postalCode` | string | no |  |
| `lines[].itemCode` | string | no |  |
| `addresses.shipFrom.line2` | string | no |  |
| `addresses.shipTo.line2` | string | no |  |
| `lines[].description` | string | no |  |
| `referenceCode` | string | no |  |
| `locationCode` | string | no |  |
| `code` | string | no |  |
| `addresses` | object | no |  |
| `commit` | boolean | no |  |
| `companyCode` | string | no |  |
| `currencyCode` | string | no |  |
| `customerCode` | string | yes |  |
| `date` | date | yes |  |
| `description` | string | no |  |
| `purchaseOrderNo` | string | no |  |
| `type` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include` | string | no | Comma-separated related objects to include in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {}
      ],
      "adjustmentDescription": "string",
      "adjustmentReason": "string",
      "batchCode": "string",
      "businessIdentificationNo": "string",
      "code": "string",
      "companyId": 1,
      "country": "string",
      "currencyCode": "string",
      "customerCode": "string",
      "customerUsageType": "string",
      "customerVendorCode": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "destinationAddressId": 1,
      "email": "ava@example.com",
      "entityUseCode": "string",
      "exchangeRate": 1,
      "exchangeRateCurrencyCode": "string",
      "exchangeRateEffectiveDate": "2026-05-07T12:00:00.000Z",
      "exemptNo": "string",
      "id": 1,
      "isSellerImporterOfRecord": true,
      "lines": [
        {}
      ],
      "locationCode": "string",
      "locationTypes": [
        {}
      ],
      "locked": true,
      "messages": [
        {}
      ],
      "modifiedDate": "2026-05-07T12:00:00.000Z",
      "modifiedUserId": 1,
      "originAddressId": 1,
      "paymentDate": "2026-05-07T12:00:00.000Z",
      "purchaseOrderNo": "string",
      "reconciled": true,
      "referenceCode": "string",
      "region": "string",
      "reportingLocationCode": "string",
      "salespersonCode": "string",
      "shippingTaxes": [
        {}
      ],
      "softwareVersion": "string",
      "status": "string",
      "summary": [
        {}
      ],
      "taxDate": "2026-05-07T12:00:00.000Z",
      "taxOverrideAmount": 1,
      "taxOverrideReason": "string",
      "taxOverrideType": "string",
      "totalAmount": 1,
      "totalDiscount": 1,
      "totalExempt": 1,
      "totalTax": 1,
      "totalTaxable": 1,
      "totalTaxCalculated": 1,
      "type": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<object> |  |
| `adjustmentDescription` | string |  |
| `adjustmentReason` | string |  |
| `batchCode` | string |  |
| `businessIdentificationNo` | string |  |
| `code` | string |  |
| `companyId` | number |  |
| `country` | string |  |
| `currencyCode` | string |  |
| `customerCode` | string |  |
| `customerUsageType` | string |  |
| `customerVendorCode` | string |  |
| `date` | date |  |
| `description` | string |  |
| `destinationAddressId` | number |  |
| `email` | string |  |
| `entityUseCode` | string |  |
| `exchangeRate` | number |  |
| `exchangeRateCurrencyCode` | string |  |
| `exchangeRateEffectiveDate` | date |  |
| `exemptNo` | string |  |
| `id` | number |  |
| `isSellerImporterOfRecord` | boolean |  |
| `lines` | array<object> |  |
| `locationCode` | string |  |
| `locationTypes` | array<object> |  |
| `locked` | boolean |  |
| `messages` | array<object> |  |
| `modifiedDate` | date |  |
| `modifiedUserId` | number |  |
| `originAddressId` | number |  |
| `paymentDate` | date |  |
| `purchaseOrderNo` | string |  |
| `reconciled` | boolean |  |
| `referenceCode` | string |  |
| `region` | string |  |
| `reportingLocationCode` | string |  |
| `salespersonCode` | string |  |
| `shippingTaxes` | array<object> |  |
| `softwareVersion` | string |  |
| `status` | string |  |
| `summary` | array<object> |  |
| `taxDate` | date |  |
| `taxOverrideAmount` | number |  |
| `taxOverrideReason` | string |  |
| `taxOverrideType` | string |  |
| `totalAmount` | number |  |
| `totalDiscount` | number |  |
| `totalExempt` | number |  |
| `totalTax` | number |  |
| `totalTaxable` | number |  |
| `totalTaxCalculated` | number |  |
| `type` | string |  |
| `version` | number |  |

## Native endpoint

Through the native Avalara AvaTax API, this operation is `POST transactions/create` (base URL `{{credentials.environment}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transaction.md) for the provider-specific parameters and requirements.

