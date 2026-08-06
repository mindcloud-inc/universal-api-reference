# Avalara AvaTax: Get Transaction By Code



```
GET https://connect.mindcloud.co/v1/universal/avalara/latest/actions/get-transaction-by-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avalara AvaTax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avalara/latest/actions/get-transaction-by-code?connectionId=$CONNECTION_ID&companyCode=string&transactionCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyCode": "string",
  "transactionCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avalara/latest/actions/get-transaction-by-code?${params}`, {
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
| `companyCode` | string | yes | Avalara company code. |
| `transactionCode` | string | yes | Avalara transaction code. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentType` | string | no | Optional document type to disambiguate transactions that share the same code. |
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

Through the native Avalara AvaTax API, this operation is `GET companies/:companyCode/transactions/:transactionCode` (base URL `{{credentials.environment}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transaction-by-code.md) for the provider-specific parameters and requirements.

