# Fluents: Create Webhook

Creates a new webhook in Fluents.

```
POST https://connect.mindcloud.co/v1/universal/fluents/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fluents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fluents/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fluents/latest/actions/create-webhook', {
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
      "account_connection_id": "string",
      "description": "string",
      "id": "string",
      "label": "string",
      "method": "string",
      "subscriptions": [
        "string"
      ],
      "url": "https://example.com",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_connection_id` | string |  |
| `description` | string |  |
| `id` | string |  |
| `label` | string |  |
| `method` | string |  |
| `subscriptions` | array<string> |  |
| `url` | string |  |
| `user_id` | string |  |

## Native endpoint

Through the native Fluents API, this operation is `POST /webhooks/create` (base URL `https://api.fluents.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

