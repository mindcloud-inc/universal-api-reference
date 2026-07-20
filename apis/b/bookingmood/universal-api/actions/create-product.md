# Bookingmood: Create Product

Creates a new product in the Bookingmood API.

```
POST https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookingmood `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name.default": "Ava Chen",
  "rentPeriod": "string",
  "timezone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name.default": "Ava Chen",
    "rentPeriod": "string",
    "timezone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name.default` | string | yes | Localized product name. |
| `rentPeriod` | string | yes | Rent period for the product. |
| `timezone` | string | yes | Timezone for the product. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ac_id": "string",
      "approximate_address": "string",
      "approximate_coordinates": {},
      "created_at": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "deleted_at": "2026-05-07T12:00:00.000Z",
      "description": {},
      "fee": {},
      "id": "string",
      "images": [
        {}
      ],
      "interaction": "string",
      "name": {},
      "organization_id": "string",
      "rent_period": "string",
      "request_status": "string",
      "services": [
        {}
      ],
      "timezone": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ac_id` | string |  |
| `approximate_address` | string |  |
| `approximate_coordinates` | object |  |
| `created_at` | date |  |
| `currency` | string |  |
| `deleted_at` | date |  |
| `description` | object |  |
| `fee` | object |  |
| `id` | string |  |
| `images` | array<object> |  |
| `interaction` | string |  |
| `name` | object |  |
| `organization_id` | string |  |
| `rent_period` | string |  |
| `request_status` | string |  |
| `services` | array<object> |  |
| `timezone` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Bookingmood API, this operation is `POST /products` (base URL `https://api.bookingmood.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

