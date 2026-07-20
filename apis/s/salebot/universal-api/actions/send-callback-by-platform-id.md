# Salebot: Send Callback by Platform ID



```
POST https://connect.mindcloud.co/v1/universal/salebot/latest/actions/send-callback-by-platform-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salebot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salebot/latest/actions/send-callback-by-platform-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "platformIds[]": [
    "string"
  ],
  "callbackText": "string",
  "groupId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salebot/latest/actions/send-callback-by-platform-id', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "platformIds[]": ["string"],
    "callbackText": "string",
    "groupId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `platformIds[]` | array<string> | yes | Messenger platform IDs to target. |
| `callbackText` | string | yes | Callback text to deliver to matching clients. |
| `groupId` | number | yes | Connected channel group ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callbackSended": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callbackSended` | number |  |

## Native endpoint

Through the native Salebot API, this operation is `POST /send_callback_by_platform_id` (base URL `https://chatter.salebot.pro/api/{{credentials.apiKey}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-callback-by-platform-id.md) for the provider-specific parameters and requirements.

