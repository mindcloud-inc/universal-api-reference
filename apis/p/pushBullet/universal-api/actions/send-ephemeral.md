# Pushbullet: Send Ephemeral

Sends an ephemeral message to the Pushbullet realtime stream.

```
POST https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/send-ephemeral
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushbullet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/send-ephemeral" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/send-ephemeral', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | Ephemeral payload type. |
| `push` | object | no | Nested push payload for ephemeral type=push. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "push": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `push` | object |  |
| `type` | string |  |

## Native endpoint

Through the native Pushbullet API, this operation is `POST /ephemerals` (base URL `https://api.pushbullet.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-ephemeral.md) for the provider-specific parameters and requirements.

