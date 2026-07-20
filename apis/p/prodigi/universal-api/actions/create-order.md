# Prodigi: Create Order

Creates and submits a new order in Prodigi.

```
POST https://connect.mindcloud.co/v1/universal/prodigi/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prodigi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prodigi/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "shippingMethod": "string",
  "recipient": {},
  "items[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prodigi/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "shippingMethod": "string",
    "recipient": {},
    "items[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `shippingMethod` | string | yes | Requested shipping method: budget, standard, standardplus, express, overnight. |
| `recipient` | object | yes | Recipient object including name and address. |
| `items[]` | array<object> | yes | Array of order items. Each item includes sku, copies, sizing, and assets. |
| `merchantReference` | string | no | Your reference for this order. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callbackUrl` | string | no | URL Prodigi can call with order progress callbacks. |
| `idempotencyKey` | string | no | Unique key that helps Prodigi detect duplicate order submissions. |
| `metadata` | object | no | Custom metadata object stored with the order. |
| `branding` | object | no | Optional branding assets such as postcard, flyer, packing slip, or stickers. |
| `packingSlip` | object | no | Optional packing slip object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "charges": [
        {}
      ],
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "items": [
        {}
      ],
      "lastUpdated": "2026-05-07T12:00:00.000Z",
      "merchantReference": "string",
      "metadata": {},
      "recipient": {},
      "shipments": [
        {}
      ],
      "shippingMethod": "string",
      "status": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `charges` | array<object> | Order charges. |
| `created` | date | Order creation timestamp. |
| `id` | string | Prodigi order ID. |
| `items` | array<object> | Order items. |
| `lastUpdated` | date | Order last updated timestamp. |
| `merchantReference` | string | Merchant order reference. |
| `metadata` | object | Merchant metadata. |
| `recipient` | object | Recipient details. |
| `shipments` | array<object> | Order shipments. |
| `shippingMethod` | string | Requested shipping method. |
| `status` | object | Order status details. |

## Native endpoint

Through the native Prodigi API, this operation is `POST /orders` (base URL `https://api.prodigi.com/v4.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

