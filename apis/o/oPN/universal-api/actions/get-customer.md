# OPN: Get Customer

Retrieves details for a customer from OPN.

```
GET https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-customer?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-customer?${params}`, {
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
| `id` | string | yes | The customer ID to retrieve. |

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

Through the native OPN API, this operation is `GET /customers/:id` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

