# Salebot: Trigger Callback



```
POST https://connect.mindcloud.co/v1/universal/salebot/latest/actions/trigger-callback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salebot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salebot/latest/actions/trigger-callback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salebot/latest/actions/trigger-callback', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | number | no | Existing Salebot client ID. |
| `clientPhone` | string | no | Phone number used to resolve the client before triggering the callback. |
| `clientEmail` | string | no | Email used to resolve the client before triggering the callback. |
| `message` | string | no | Callback text to inject into the bot flow. |
| `resumeBot` | boolean | no | Resume a paused bot before delivering the callback. |

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

Through the native Salebot API, this operation is `POST /callback` (base URL `https://chatter.salebot.pro/api/{{credentials.apiKey}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trigger-callback.md) for the provider-specific parameters and requirements.

