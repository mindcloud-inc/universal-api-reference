# Paddle: Create Product

Creates a new product in Paddle.

```
POST https://connect.mindcloud.co/v1/universal/paddle/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paddle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/paddle/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paddle/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "custom_data": {
        "features": {
          "aircraft_performance": true,
          "compliance_monitoring": true,
          "flight_log_management": true,
          "payment_by_invoice": true,
          "route_planning": true,
          "sso": true
        },
        "suggested_addons": [
          [
            "string"
          ]
        ],
        "upgrade_description": "string"
      },
      "description": "string",
      "id": "string",
      "image_url": "https://example.com",
      "name": "Ava Chen",
      "status": "string",
      "tax_category": "string",
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `custom_data.features.aircraft_performance` | boolean |  |
| `custom_data.features.compliance_monitoring` | boolean |  |
| `custom_data.features.flight_log_management` | boolean |  |
| `custom_data.features.payment_by_invoice` | boolean |  |
| `custom_data.features.route_planning` | boolean |  |
| `custom_data.features.sso` | boolean |  |
| `custom_data.suggested_addons[]` | array<string> |  |
| `custom_data.upgrade_description` | string |  |
| `description` | string |  |
| `id` | string |  |
| `image_url` | string |  |
| `name` | string |  |
| `status` | string |  |
| `tax_category` | string |  |
| `type` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Paddle API, this operation is `POST products` (base URL `https://api.paddle.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

