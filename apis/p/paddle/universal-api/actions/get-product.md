# Paddle: Get Product

Retrieves a product from Paddle.

```
GET https://connect.mindcloud.co/v1/universal/paddle/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paddle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paddle/latest/actions/get-product?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paddle/latest/actions/get-product?${params}`, {
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
| `productId` | string | no |  |

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

Through the native Paddle API, this operation is `GET products/{product_id}` (base URL `https://api.paddle.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

