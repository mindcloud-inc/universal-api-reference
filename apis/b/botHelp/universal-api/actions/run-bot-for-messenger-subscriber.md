# BotHelp: Run Bot For Messenger Subscriber

Runs a bot for a subscriber by Facebook Messenger user ID in BotHelp.

```
PUT https://connect.mindcloud.co/v1/universal/botHelp/latest/actions/run-bot-for-messenger-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BotHelp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/botHelp/latest/actions/run-bot-for-messenger-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "botReferral": "string",
  "messenger_user_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botHelp/latest/actions/run-bot-for-messenger-subscriber', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "botReferral": "string",
    "messenger_user_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botReferral` | string | yes | Bot referral to start for the subscriber. |
| `messenger_user_id` | string | yes | Facebook Messenger user PSID. |
| `stepReferral` | string | no | Optional bot step referral to start at a specific step. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the request succeeded. |

## Native endpoint

Through the native BotHelp API, this operation is `POST /v2/subscribers/messenger/:messenger_user_id/bot` (base URL `https://api.bothelp.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-bot-for-messenger-subscriber.md) for the provider-specific parameters and requirements.

