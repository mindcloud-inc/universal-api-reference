# OPN: Update Customer

Updates an existing customer in OPN.

```
PUT https://connect.mindcloud.co/v1/universal/oPN/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oPN/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | The updated customer description. |
| `email` | string | no | The updated customer email address. |
| `id` | string | yes | The customer ID to update. |

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

Through the native OPN API, this operation is `PATCH /customers/:id` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

