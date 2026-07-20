# Copperx: Get Invoice

Retrieves invoice record details from Copperx.

```
GET https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Copperx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-invoice?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-invoice?${params}`, {
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
| `id` | string | yes | Invoice ID path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowPromotionCodes": true,
      "autoAdvance": true,
      "billingReason": "string",
      "collectionMethod": "string",
      "createdAt": "string",
      "currency": "string",
      "customer": {},
      "customerId": "string",
      "description": "string",
      "id": "string",
      "invoiceNumber": "string",
      "invoiceType": "string",
      "lineItems": {},
      "metadata": {},
      "organizationId": "string",
      "paid": true,
      "paymentSetting": {},
      "paymentSettingId": "string",
      "status": "string",
      "subscriptionId": "string",
      "subTotal": "string",
      "taxRateIds": [
        "string"
      ],
      "total": "string",
      "totalTax": "string",
      "updatedAt": "string",
      "url": "https://example.com",
      "visibility": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowPromotionCodes` | boolean |  |
| `autoAdvance` | boolean |  |
| `billingReason` | string |  |
| `collectionMethod` | string |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `customer` | object |  |
| `customerId` | string |  |
| `description` | string |  |
| `id` | string |  |
| `invoiceNumber` | string |  |
| `invoiceType` | string |  |
| `lineItems` | object |  |
| `metadata` | object |  |
| `organizationId` | string |  |
| `paid` | boolean |  |
| `paymentSetting` | object |  |
| `paymentSettingId` | string |  |
| `status` | string |  |
| `subscriptionId` | string |  |
| `subTotal` | string |  |
| `taxRateIds` | array<string> |  |
| `total` | string |  |
| `totalTax` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |
| `visibility` | number |  |

## Native endpoint

Through the native Copperx API, this operation is `GET /invoices/{id}` (base URL `https://api.copperx.dev/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice.md) for the provider-specific parameters and requirements.

