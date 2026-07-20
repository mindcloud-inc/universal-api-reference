# OPN: Create Customer

Creates a new customer in OPN.

```
POST https://connect.mindcloud.co/v1/universal/oPN/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oPN/latest/actions/create-customer', {
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
| `description` | string | no | The customer description. |
| `email` | string | no | The customer email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cards": {},
      "created_at": "string",
      "default_card": "string",
      "deleted": true,
      "description": "string",
      "email": "ava@example.com",
      "id": "string",
      "linked_accounts": {},
      "livemode": true,
      "location": "string",
      "metadata": {},
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cards` | object |  |
| `created_at` | string |  |
| `default_card` | string |  |
| `deleted` | boolean |  |
| `description` | string |  |
| `email` | string |  |
| `id` | string |  |
| `linked_accounts` | object |  |
| `livemode` | boolean |  |
| `location` | string |  |
| `metadata` | object |  |
| `object` | string |  |

## Native endpoint

Through the native OPN API, this operation is `POST /customers` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

