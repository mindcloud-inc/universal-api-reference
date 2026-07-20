# Voucherify: Create Customer

Creates a new customer in Voucherify, or updates an existing one.

```
POST https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voucherify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/create-customer', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceId` | string | no | External customer identifier. |
| `name` | string | no | Customer display name. |
| `email` | string | no | Customer email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "createdAt": "string",
      "description": "string",
      "email": "ava@example.com",
      "id": "string",
      "loyalty": {},
      "metadata": {},
      "name": "Ava Chen",
      "object": "string",
      "referrals": {},
      "sourceId": "string",
      "summary": {},
      "systemMetadata": {},
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `createdAt` | string |  |
| `description` | string |  |
| `email` | string |  |
| `id` | string |  |
| `loyalty` | object |  |
| `metadata` | object |  |
| `name` | string |  |
| `object` | string |  |
| `referrals` | object |  |
| `sourceId` | string |  |
| `summary` | object |  |
| `systemMetadata` | object |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Voucherify API, this operation is `POST /customers` (base URL `https://us1.api.voucherify.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

