# Tolq: Order a Quoted Request

Orders a quoted translation request in Tolq.

```
POST https://connect.mindcloud.co/v1/universal/tolq/latest/actions/order-a-quoted-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tolq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tolq/latest/actions/order-a-quoted-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "3"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tolq/latest/actions/order-a-quoted-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "3"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Quoted Tolq request ID to confirm. Example: `3`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "callback_response_code": 1,
      "completed_at": "2026-05-07T12:00:00.000Z",
      "context_url": "https://example.com",
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "last_callback_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "orders": [
        {}
      ],
      "original": {},
      "quality": "string",
      "slug": "string",
      "source_language_code": "string",
      "status": "string",
      "style_guide_reference_id": 1,
      "target_language_code": "string",
      "total_cost": 1,
      "total_keys": 1,
      "total_ordered_words": 1,
      "total_orders": 1,
      "total_words": 1,
      "translations": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object |  |
| `callback_response_code` | number |  |
| `completed_at` | date |  |
| `context_url` | string |  |
| `created_at` | date |  |
| `description` | string |  |
| `id` | number |  |
| `last_callback_at` | date |  |
| `name` | string |  |
| `orders` | array<object> |  |
| `original` | object |  |
| `quality` | string |  |
| `slug` | string |  |
| `source_language_code` | string |  |
| `status` | string |  |
| `style_guide_reference_id` | number |  |
| `target_language_code` | string |  |
| `total_cost` | number |  |
| `total_keys` | number |  |
| `total_ordered_words` | number |  |
| `total_orders` | number |  |
| `total_words` | number |  |
| `translations` | object |  |

## Native endpoint

Through the native Tolq API, this operation is `POST /translations/requests/:id/order` (base URL `https://api.tolq.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/order-a-quoted-request.md) for the provider-specific parameters and requirements.

