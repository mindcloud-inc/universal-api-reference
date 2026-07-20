# Copperx: Void Invoice

Voids an existing invoice in Copperx.

```
PUT https://connect.mindcloud.co/v1/universal/copperx/latest/actions/void-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Copperx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/copperx/latest/actions/void-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/copperx/latest/actions/void-invoice', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Invoice ID path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
      "subTotal": "string",
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
| `subTotal` | string |  |
| `total` | string |  |
| `totalTax` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |
| `visibility` | number |  |

## Native endpoint

Through the native Copperx API, this operation is `POST /invoices/{id}/void` (base URL `https://api.copperx.dev/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/void-invoice.md) for the provider-specific parameters and requirements.

