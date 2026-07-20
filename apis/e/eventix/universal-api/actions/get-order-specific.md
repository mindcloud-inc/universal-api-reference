# Eventix: Get an entire specific Order

Retrieves a specific order from Eventix.

```
GET https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-order-specific
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-order-specific?connectionId=$CONNECTION_ID&guid=order-guid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "guid": "order-guid"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-order-specific?${params}`, {
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
| `guid` | string | yes | The guid of the Order. Example: `order-guid`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "download_link": "https://example.com",
      "download_ready": true,
      "email": "ava@example.com",
      "finn_original_price": 1,
      "finn_price": 1,
      "finn_service_fee": 1,
      "finn_value": 1,
      "firstName": "Ava",
      "fullname": "Ava Chen",
      "guid": "string",
      "has_receipt": true,
      "invalidated_reason": "string",
      "invalidated_since": "2026-05-07T12:00:00.000Z",
      "is_complete": true,
      "is_seated": true,
      "lastName": "Chen",
      "locale": "string",
      "payments": [
        {}
      ],
      "pdf_rendered": true,
      "products": [
        {}
      ],
      "purchase_channel": "string",
      "receipt_link": "https://example.com",
      "refunds": [
        {}
      ],
      "send_email": true,
      "shop": {},
      "shop_id": "string",
      "status": "string",
      "tickets": [
        {}
      ],
      "transaction_fee": 1,
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `created_at` | date |  |
| `download_link` | string |  |
| `download_ready` | boolean |  |
| `email` | string |  |
| `finn_original_price` | number |  |
| `finn_price` | number |  |
| `finn_service_fee` | number |  |
| `finn_value` | number |  |
| `firstName` | string |  |
| `fullname` | string |  |
| `guid` | string |  |
| `has_receipt` | boolean |  |
| `invalidated_reason` | string |  |
| `invalidated_since` | date |  |
| `is_complete` | boolean |  |
| `is_seated` | boolean |  |
| `lastName` | string |  |
| `locale` | string |  |
| `payments` | array<object> |  |
| `pdf_rendered` | boolean |  |
| `products` | array<object> |  |
| `purchase_channel` | string |  |
| `receipt_link` | string |  |
| `refunds` | array<object> |  |
| `send_email` | boolean |  |
| `shop` | object |  |
| `shop_id` | string |  |
| `status` | string |  |
| `tickets` | array<object> |  |
| `transaction_fee` | number |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Eventix API, this operation is `GET /3.0.0/order/:guid` (base URL `https://api.weeztix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-specific.md) for the provider-specific parameters and requirements.

