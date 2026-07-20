# Lulu: Create Webhook

Creates a new webhook in Lulu.

```
POST https://connect.mindcloud.co/v1/universal/lulu/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lulu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lulu/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "topics[]": [
    "PRINT_JOB_STATUS_CHANGED"
  ],
  "url": "https://example.com/lulu/webhook"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lulu/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "topics[]": ["PRINT_JOB_STATUS_CHANGED"],
    "url": "https://example.com/lulu/webhook"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `topics[]` | array | yes | List of Lulu webhook topics to subscribe to. Default: `["PRINT_JOB_STATUS_CHANGED"]`. |
| `url` | string | yes | Destination URL for Lulu webhook deliveries. Default: `https://example.com/lulu/webhook`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "isActive": true,
      "topics": [
        "string"
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `isActive` | boolean |  |
| `topics` | array<string> |  |
| `url` | string |  |

## Native endpoint

Through the native Lulu API, this operation is `POST /webhooks/` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

