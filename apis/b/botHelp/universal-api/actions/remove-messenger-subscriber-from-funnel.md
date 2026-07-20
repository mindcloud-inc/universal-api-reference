# BotHelp: Remove Messenger Subscriber From Funnel

Removes a subscriber from a funnel by Facebook Messenger user ID in BotHelp.

```
PUT https://connect.mindcloud.co/v1/universal/botHelp/latest/actions/remove-messenger-subscriber-from-funnel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BotHelp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/botHelp/latest/actions/remove-messenger-subscriber-from-funnel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messenger_user_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botHelp/latest/actions/remove-messenger-subscriber-from-funnel', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messenger_user_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `funnelReferral` | string | no | Optional sequence/funnel referral to remove. |
| `messenger_user_id` | string | yes | Facebook Messenger user PSID. |

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

Through the native BotHelp API, this operation is `DELETE /v2/subscribers/messenger/:messenger_user_id/funnel` (base URL `https://api.bothelp.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-messenger-subscriber-from-funnel.md) for the provider-specific parameters and requirements.

