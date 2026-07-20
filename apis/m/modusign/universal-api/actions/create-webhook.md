# Modusign: Create Webhook

Creates a new webhook in Modusign.

```
POST https://connect.mindcloud.co/v1/universal/modusign/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Modusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/modusign/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/modusign/latest/actions/create-webhook', {
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
      "createdAt": "string",
      "events": [
        "string"
      ],
      "headers": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | The creation timestamp. |
| `events` | array<string> | Subscribed webhook events. |
| `headers` | array<object> | Additional webhook headers. |
| `id` | string | The webhook ID. |
| `name` | string | The webhook name. |
| `updatedAt` | string | The update timestamp. |
| `url` | string | The webhook callback URL. |

## Native endpoint

Through the native Modusign API, this operation is `POST /webhooks` (base URL `https://api.modusign.co.kr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

