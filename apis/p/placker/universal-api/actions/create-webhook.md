# Placker: Create Webhook



```
POST https://connect.mindcloud.co/v1/universal/placker/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/placker/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "board": "1235",
  "notificationUrl": "https://example.com/hook",
  "events[]": "card_created"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/placker/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "board": "1235",
    "notificationUrl": "https://example.com/hook",
    "events[]": "card_created"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `board` | number | yes | Board ID. Example: `1235`. |
| `notificationUrl` | string | yes | Webhook target URL. Example: `https://example.com/hook`. |
| `events[]` | array<string> | yes | Event types to subscribe to. Example: `card_created`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "board": 1,
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `board` | number | Board ID for the webhook. |
| `id` | string | ID of the newly created webhook. |

## Native endpoint

Through the native Placker API, this operation is `POST /webhook/:board` (base URL `https://api.placker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

