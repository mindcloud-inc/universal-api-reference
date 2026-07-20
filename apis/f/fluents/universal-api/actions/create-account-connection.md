# Fluents: Create Account Connection

Creates a new account connection in Fluents.

```
POST https://connect.mindcloud.co/v1/universal/fluents/latest/actions/create-account-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fluents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fluents/latest/actions/create-account-connection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fluents/latest/actions/create-account-connection', {
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
      "account_supports_any_caller_id": true,
      "config": {},
      "credentials": {},
      "description": "string",
      "id": "string",
      "label": "string",
      "steering_pool": [
        "string"
      ],
      "type": "string",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_supports_any_caller_id` | boolean |  |
| `config` | object |  |
| `credentials` | object |  |
| `description` | string |  |
| `id` | string |  |
| `label` | string |  |
| `steering_pool` | array<string> |  |
| `type` | string |  |
| `user_id` | string |  |

## Native endpoint

Through the native Fluents API, this operation is `POST /account_connections/create` (base URL `https://api.fluents.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-account-connection.md) for the provider-specific parameters and requirements.

