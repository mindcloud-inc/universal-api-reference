# Botbaba: Create Bot User



```
POST https://connect.mindcloud.co/v1/universal/botbaba/latest/actions/create-bot-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botbaba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/botbaba/latest/actions/create-bot-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "botId": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botbaba/latest/actions/create-bot-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "botId": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botId` | number | yes | Bot identifier. |
| `name` | string | yes | Bot user name. |
| `mobile` | string | no | Bot user mobile number. |
| `email` | string | no | Bot user email. |
| `gender` | string | no | Bot user gender. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "botUserId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `botUserId` | number |  |

## Native endpoint

Through the native Botbaba API, this operation is `POST /api/InsertBotUser` (base URL `https://app.botbaba.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bot-user.md) for the provider-specific parameters and requirements.

