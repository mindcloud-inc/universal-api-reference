# Fluents: Update Account Connection

Updates an existing account connection in Fluents.

```
PUT https://connect.mindcloud.co/v1/universal/fluents/latest/actions/update-account-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fluents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fluents/latest/actions/update-account-connection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fluents/latest/actions/update-account-connection', {
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
| `id` | string | yes | Fluents account connection ID. |

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

Through the native Fluents API, this operation is `POST /account_connections/update` (base URL `https://api.fluents.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-account-connection.md) for the provider-specific parameters and requirements.

