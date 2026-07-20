# Prodigi: Get Order

Retrieves details for a specific Prodigi order.

```
GET https://connect.mindcloud.co/v1/universal/prodigi/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prodigi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prodigi/latest/actions/get-order?connectionId=$CONNECTION_ID&prodigiOrderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "prodigiOrderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prodigi/latest/actions/get-order?${params}`, {
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
| `prodigiOrderId` | string | yes | Prodigi order ID, such as ord_123456. |

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

Through the native Prodigi API, this operation is `GET /orders/[:prodigiOrderId]` (base URL `https://api.prodigi.com/v4.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

