# Tolstoy: Add Webhook

Creates a new webhook in Tolstoy.

```
POST https://connect.mindcloud.co/v1/universal/tolstoy/latest/actions/add-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tolstoy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tolstoy/latest/actions/add-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "event": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tolstoy/latest/actions/add-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "event": "string",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `event` | string | yes | The event you want to subscribe to |
| `url` | string | yes | The url to send the event to |

## Response

```json
{
  "success": true,
  "data": [
    {
      "__typename": "Ava Chen",
      "appKey": "string",
      "createdAt": "string",
      "event": "string",
      "id": "string",
      "owner": "string",
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
| `__typename` | string |  |
| `appKey` | string |  |
| `createdAt` | string |  |
| `event` | string |  |
| `id` | string |  |
| `owner` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Tolstoy API, this operation is `POST /webhooks/` (base URL `https://api.gotolstoy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-webhook.md) for the provider-specific parameters and requirements.

