# Mocean API: Send Verify Code Telegram



```
POST https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/send-verify-code-telegram
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mocean API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/send-verify-code-telegram" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "botUsername": "Ava Chen",
  "brand": "string",
  "chatId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/send-verify-code-telegram', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "botUsername": "Ava Chen",
    "brand": "string",
    "chatId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botUsername` | string | yes | Telegram bot username. |
| `brand` | string | yes | Brand or application name for the verification message. |
| `chatId` | string | yes | Telegram chat ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "botUsername": "Ava Chen",
      "chatId": "string",
      "error": "string",
      "requestId": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `botUsername` | string |  |
| `chatId` | string |  |
| `error` | string |  |
| `requestId` | string |  |
| `status` | number |  |

## Native endpoint

Through the native Mocean API API, this operation is `POST /rest/2/verify/req/telegram?mocean-resp-format=json` (base URL `https://rest.moceanapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-verify-code-telegram.md) for the provider-specific parameters and requirements.

