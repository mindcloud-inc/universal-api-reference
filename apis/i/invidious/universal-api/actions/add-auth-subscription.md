# Invidious: Add Auth Subscription



```
POST https://connect.mindcloud.co/v1/universal/invidious/latest/actions/add-auth-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invidious `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/invidious/latest/actions/add-auth-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelId": "UC_x5XG1OV2P6uZZ5FSM9Ttw"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/invidious/latest/actions/add-auth-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelId": "UC_x5XG1OV2P6uZZ5FSM9Ttw"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelId` | string | yes | Channel UCID to subscribe to. Example: `UC_x5XG1OV2P6uZZ5FSM9Ttw`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorId": "string",
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
| `authorId` | string |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Invidious API, this operation is `POST /auth/subscriptions/:ucid` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-auth-subscription.md) for the provider-specific parameters and requirements.

