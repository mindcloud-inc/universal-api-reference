# Zoho Books: Get Estimate



```
GET https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/get-estimate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Books `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/get-estimate?connectionId=$CONNECTION_ID&estimateId=string&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "estimateId": "string",
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/get-estimate?${params}`, {
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
| `estimateId` | list | yes |  |
| `organizationId` | list | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `print` | boolean | no |  |
| `accept` | list | no | One of: `0`, `1`, `2`. |

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

Through the native Zoho Books API, this operation is `GET /estimates/:estimate_id` (base URL `https://www.zohoapis.com/books/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-estimate.md) for the provider-specific parameters and requirements.

