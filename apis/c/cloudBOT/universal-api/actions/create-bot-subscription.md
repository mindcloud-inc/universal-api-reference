# Cloud BOT: Create Bot Subscription

Creates a bot subscription in Cloud BOT.

```
POST https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/create-bot-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloud BOT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/create-bot-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "publicId": "string",
  "botId": "string",
  "event": "string",
  "callbackType": "webhook",
  "callbackEndpoint": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/create-bot-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "publicId": "string",
    "botId": "string",
    "event": "string",
    "callbackType": "webhook",
    "callbackEndpoint": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `publicId` | string | yes |  |
| `botId` | string | yes |  |
| `event` | string | yes |  |
| `callbackType` | string | yes | Default: `webhook`. |
| `callbackEndpoint` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "subscribeId": 1,
      "unsubscribeEndpoint": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Response status code |
| `subscribeId` | number | Created subscription ID |
| `unsubscribeEndpoint` | string | Endpoint used to unsubscribe |

## Native endpoint

Through the native Cloud BOT API, this operation is `POST /:public_id/bots/:bot_id/subscriptions` (base URL `https://api.c-bot.pro`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bot-subscription.md) for the provider-specific parameters and requirements.

