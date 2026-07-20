# LinkedCamp: Create Webhook



```
POST https://connect.mindcloud.co/v1/universal/linkedCamp/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkedCamp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linkedCamp/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "callbackUrl": "https://example.com",
  "title": "string",
  "event": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkedCamp/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "callbackUrl": "https://example.com",
    "title": "string",
    "event": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callbackUrl` | string | yes | Webhook callback URL. |
| `title` | string | yes | Webhook title. |
| `event` | string | yes | Webhook event: CONNECT_INVITED, ACCEPTS_REQUEST, REPLY_DETECTED, EMAIL_SENT, OPENED, BOUNCED, CLICKED, or UNSUBSCRIBED. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider response message. |
| `success` | boolean | Whether the request succeeded. |

## Native endpoint

Through the native LinkedCamp API, this operation is `POST /webhooks` (base URL `https://api.linkedcamp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

