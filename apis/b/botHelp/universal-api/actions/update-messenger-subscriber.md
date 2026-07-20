# BotHelp: Update Messenger Subscriber

Updates a subscriber by Facebook Messenger user ID in BotHelp.

```
PUT https://connect.mindcloud.co/v1/universal/botHelp/latest/actions/update-messenger-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BotHelp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/botHelp/latest/actions/update-messenger-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messenger_user_id": "string",
  "operations[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botHelp/latest/actions/update-messenger-subscriber', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messenger_user_id": "string",
    "operations[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messenger_user_id` | string | yes | Facebook Messenger user PSID. |
| `operations[]` | array<object> | yes | JSON Patch operations array for tags or common subscriber fields. |

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

Through the native BotHelp API, this operation is `PATCH /v2/subscribers/messenger/:messenger_user_id` (base URL `https://api.bothelp.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-messenger-subscriber.md) for the provider-specific parameters and requirements.

