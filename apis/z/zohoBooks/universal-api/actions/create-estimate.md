# Zoho Books: Create Estimate



```
POST https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/create-estimate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Books `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/create-estimate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "string",
  "customerId": "string",
  "lineItems[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/create-estimate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "string",
    "customerId": "string",
    "lineItems[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | list | yes |  |
| `send` | boolean | no |  |
| `customerId` | list | yes |  |
| `estimateNumber` | string | no | Example: `EST-STAGE3-20260311`. |
| `referenceNumber` | string | no | Example: `REF-STAGE3-20260311`. |
| `date` | date | no | Example: `2026-03-11`. |
| `expiryDate` | date | no | Example: `2026-03-31`. |
| `lineItems[]` | array<object> | yes |  |
| `lineItems[].itemId` | list | no |  |
| `lineItems[].rate` | number | no | Example: `150`. |
| `lineItems[].quantity` | number | no | Example: `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ignoreAutoNumberGeneration` | boolean | no |  |
| `discount` | string | no | Example: `10%`. |
| `isDiscountBeforeTax` | boolean | no |  |
| `discountType` | list | no | One of: `0`, `1`. |
| `isInclusiveTax` | boolean | no |  |
| `notes` | string | no | Example: `Prepared by Codex for Stage 3 validation.`. |
| `terms` | string | no | Example: `Valid for 30 days.`. |
| `shippingCharge` | number | no | Example: `5`. |
| `adjustment` | number | no | Example: `0`. |
| `adjustmentDescription` | string | no | Example: `Round-off`. |
| `locationId` | string | no | Example: `1234567890`. |
| `projectId` | string | no | Example: `1234567890`. |
| `acceptRetainer` | boolean | no |  |
| `retainerPercentage` | number | no | Example: `25`. |
| `lineItems[].name` | string | no | Example: `Codex Stage3 Item 20260311 Updated`. |
| `lineItems[].description` | string | no | Example: `Updated during Zoho Books Stage 3 validation`. |
| `lineItems[].discountAmount` | number | no | Example: `0`. |
| `lineItems[].discount` | string | no | Example: `0%`. |
| `lineItems[].locationId` | string | no | Example: `1234567890`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adjustment": 1,
      "createdTime": "string",
      "currencyCode": "string",
      "currencyId": "string",
      "customerId": "string",
      "customerName": "Ava Chen",
      "date": "2026-05-07T12:00:00.000Z",
      "discount": 1,
      "discountType": "string",
      "estimateId": "string",
      "estimateNumber": "string",
      "exchangeRate": 1,
      "expiryDate": "string",
      "isDiscountBeforeTax": true,
      "isInclusiveTax": true,
      "lastModifiedTime": "string",
      "lineItems": [
        {}
      ],
      "notes": "string",
      "referenceNumber": "string",
      "shippingCharge": 1,
      "status": "string",
      "subTotal": 1,
      "tags": [
        {}
      ],
      "taxTotal": 1,
      "templateId": "string",
      "templateName": "Ava Chen",
      "terms": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adjustment` | number | Adjustment amount. |
| `createdTime` | string | Creation timestamp. |
| `currencyCode` | string | Currency code. |
| `currencyId` | string | Currency identifier. |
| `customerId` | string | Customer identifier. |
| `customerName` | string | Customer name. |
| `date` | date | Estimate date. |
| `discount` | number | Applied discount value. |
| `discountType` | string | Discount application mode. |
| `estimateId` | string | Unique identifier of the estimate. |
| `estimateNumber` | string | Estimate number. |
| `exchangeRate` | number | Exchange rate for the estimate. |
| `expiryDate` | string | Expiry date when present. |
| `isDiscountBeforeTax` | boolean | Whether discount is applied before tax. |
| `isInclusiveTax` | boolean | Whether taxes are inclusive. |
| `lastModifiedTime` | string | Last modification timestamp. |
| `lineItems` | array<object> | Line items included in the estimate. |
| `notes` | string | Customer-facing notes. |
| `referenceNumber` | string | External reference number. |
| `shippingCharge` | number | Shipping charge amount. |
| `status` | string | Estimate status. |
| `subTotal` | number | Subtotal amount. |
| `tags` | array<object> | Tags associated with the estimate. |
| `taxTotal` | number | Tax total amount. |
| `templateId` | string | Template identifier. |
| `templateName` | string | Template name. |
| `terms` | string | Terms for the estimate. |
| `total` | number | Total amount. |

## Native endpoint

Through the native Zoho Books API, this operation is `POST /estimates` (base URL `https://www.zohoapis.com/books/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-estimate.md) for the provider-specific parameters and requirements.

