# JANDI: Send Incoming Webhook Message



```
POST https://connect.mindcloud.co/v1/universal/jANDI/latest/actions/send-incoming-webhook-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JANDI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jANDI/latest/actions/send-incoming-webhook-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": "MindCloud test message"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jANDI/latest/actions/send-incoming-webhook-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": "MindCloud test message"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | string | yes | The main JANDI message text. This is the only required field. Example: `MindCloud test message`. |
| `connectColor` | string | no | Optional hex color for the attachment bar. Example: `#FAC11B`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `connectInfo[]` | array<object> | no | Optional attachment items to include below the message body. Example: `[object Object]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native JANDI API returns.

## Native endpoint

Through the native JANDI API, this operation is `POST {{credentials.incomingWebhookUrl}}` (base URL `https://wh.jandi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-incoming-webhook-message.md) for the provider-specific parameters and requirements.

