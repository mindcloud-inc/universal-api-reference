# Dukaan: Create Customer

Creates a new customer in Dukaan.

```
POST https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dukaan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Sample Customer",
  "mobile": "+91-9999999998",
  "store": "102712269"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Sample Customer",
    "mobile": "+91-9999999998",
    "store": "102712269"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Customer name. Example: `Sample Customer`. |
| `email` | string | no | Customer email address. Example: `customer@example.com`. |
| `mobile` | string | yes | Customer mobile number. Example: `+91-9999999998`. |
| `store` | number | yes | Store ID for the customer. Example: `102712269`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address_line": "string",
      "city": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": 1,
      "mobile": "string",
      "modified_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "notes": "string",
      "orders_count": 1,
      "orders_total_cost": 1,
      "pin": "string",
      "state": "string",
      "tags": [
        {}
      ],
      "type": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address_line` | string | Customer address line |
| `city` | string | Customer city |
| `created_at` | date | Creation timestamp |
| `email` | string | Customer email address |
| `id` | number | Dukaan customer or audience record ID |
| `mobile` | string | Customer mobile number |
| `modified_at` | date | Last modified timestamp |
| `name` | string | Customer name |
| `notes` | string | Customer notes |
| `orders_count` | number | Customer order count |
| `orders_total_cost` | number | Total customer order value |
| `pin` | string | Customer postal code |
| `state` | string | Customer state |
| `tags` | array<object> | Customer tags |
| `type` | string | Customer type |
| `uuid` | string | Dukaan customer UUID |

## Native endpoint

Through the native Dukaan API, this operation is `POST api/campaign/seller/store-lead/v2/` (base URL `https://api.mydukaan.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

