# BotHelp: Stop Bot For Subscriber

Stops a bot for a subscriber in BotHelp.

```
PUT https://connect.mindcloud.co/v1/universal/botHelp/latest/actions/stop-bot-for-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BotHelp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/botHelp/latest/actions/stop-bot-for-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriber_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botHelp/latest/actions/stop-bot-for-subscriber', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriber_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botReferral` | string | no | Optional bot referral to stop. |
| `subscriber_id` | string | yes | BotHelp subscriber ID. |

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

Through the native BotHelp API, this operation is `DELETE /v1/subscribers/:subscriber_id/bot` (base URL `https://api.bothelp.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stop-bot-for-subscriber.md) for the provider-specific parameters and requirements.

