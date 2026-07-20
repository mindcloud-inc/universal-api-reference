# QWIC: Set Events Webhook URL

Updates the events webhook URL in QWIC.

```
PUT https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/set-events-webhook-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QWIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/set-events-webhook-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "webhookUrl": "https://example.com",
  "subscribedEvents[]": [
    {}
  ],
  "isEnabled": true,
  "token": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/set-events-webhook-url', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "webhookUrl": "https://example.com",
    "subscribedEvents[]": [{}],
    "isEnabled": true,
    "token": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | The account ID. |
| `webhookUrl` | string | yes | The webhook endpoint URL. |
| `subscribedEvents[]` | array<object> | yes | The subscribed event objects. |
| `isEnabled` | boolean | yes | Whether the webhook is enabled. |
| `token` | string | yes | The webhook verification token. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native QWIC API, this operation is `POST /v1/accounts/:account_id/webhook` (base URL `https://app.qwic.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-events-webhook-url.md) for the provider-specific parameters and requirements.

