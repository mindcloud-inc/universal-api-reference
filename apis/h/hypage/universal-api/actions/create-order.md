# Hy.page: Create Order



```
POST https://connect.mindcloud.co/v1/universal/hypage/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hy.page `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hypage/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "amount": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hypage/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "amount": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Person email; creates the person if new. |
| `notes` | string | no | Order notes. |
| `source` | string | no | Order source. |
| `amount` | number | yes | Order amount. |
| `currency` | string | no | Order currency. |
| `name` | string | no | Person name. |
| `orderId` | string | no | External order ID; used for deduplication if provided. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `isTest` | boolean | no | Whether the order is a test order. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "id": "string",
      "isNew": true,
      "isTest": true,
      "orderNumber": "string",
      "paymentStatus": "string",
      "peopleId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `id` | string |  |
| `isNew` | boolean |  |
| `isTest` | boolean |  |
| `orderNumber` | string |  |
| `paymentStatus` | string |  |
| `peopleId` | string |  |

## Native endpoint

Through the native Hy.page API, this operation is `POST /hyax-api/v1/orders` (base URL `https://platform.hyax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

