# SMS.to: Send Viber Message

Sends a single Viber message through SMS.to.

```
POST https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/send-viber-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS.to `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/send-viber-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/send-viber-message', {
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
| `message` | string | no | Your message. |
| `to` | string | no | Phone number. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callbackUrl` | string | no | A callback URL for message status updates. |
| `viberImageUrl` | string | no | Image URL to Viber. |
| `viberTargetUrl` | string | no | Target URL. |
| `viberCaption` | string | no | Message caption. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "messageId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `messageId` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native SMS.to API, this operation is `POST /viber/send` (base URL `https://api.sms.to`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-viber-message.md) for the provider-specific parameters and requirements.

