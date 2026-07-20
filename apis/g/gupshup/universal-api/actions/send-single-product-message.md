# Gupshup: Send Single Product Message

Sends a single product WhatsApp message through Gupshup.

```
POST https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/send-single-product-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gupshup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/send-single-product-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/send-single-product-message', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "messageId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `messageId` | string | Gupshup unique message identifier for the submitted message. |
| `status` | string | Submission status returned by Gupshup. |

## Native endpoint

Through the native Gupshup API, this operation is `POST /wa/api/v1/msg` (base URL `https://api.gupshup.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-single-product-message.md) for the provider-specific parameters and requirements.

