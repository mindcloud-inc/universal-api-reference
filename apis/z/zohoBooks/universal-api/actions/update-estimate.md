# Zoho Books: Update Estimate



```
PUT https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/update-estimate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Books `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/update-estimate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "estimateId": "string",
  "organizationId": "string",
  "customerId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/update-estimate', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "estimateId": "string",
    "organizationId": "string",
    "customerId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `estimateId` | list | yes |  |
| `organizationId` | list | yes |  |
| `customerId` | list | yes |  |
| `estimateNumber` | string | no | Unique identifier for the estimate when overriding auto numbering. Example: `QT-000001`. |
| `referenceNumber` | string | no | Example: `REF-STAGE3-20260311-UPD`. |
| `date` | date | no | Date the estimate is created in YYYY-MM-DD format. Example: `2026-03-11`. |
| `expiryDate` | date | no | Date when the estimate expires in YYYY-MM-DD format. Example: `2026-03-31`. |
| `lineItems[]` | array<object> | no |  |
| `lineItems[].lineItemId` | string | no | Example: `1234567890`. |
| `lineItems[].itemId` | list | no |  |
| `lineItems[].rate` | number | no | Unit price for the line item. Example: `175`. |
| `lineItems[].quantity` | number | no | Number of units for the line item. Example: `2`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ignoreAutoNumberGeneration` | boolean | no |  |
| `notes` | string | no | Example: `Updated during Zoho Books Stage 3 validation.`. |
| `lineItems[].description` | string | no | Example: `Estimate updated during Zoho Books Stage 3 validation`. |

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

Through the native Zoho Books API, this operation is `PUT /estimates/:estimate_id` (base URL `https://www.zohoapis.com/books/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-estimate.md) for the provider-specific parameters and requirements.

