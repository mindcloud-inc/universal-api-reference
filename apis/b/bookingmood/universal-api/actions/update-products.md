# Bookingmood: Update Products

Updates product records in the Bookingmood API.

```
PUT https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/update-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookingmood `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/update-products" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "name.default": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/update-products', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "name.default": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Filter the product by id using PostgREST syntax. |
| `name.default` | string | yes | Localized product name. |

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

Through the native Bookingmood API, this operation is `PATCH /products` (base URL `https://api.bookingmood.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-products.md) for the provider-specific parameters and requirements.

