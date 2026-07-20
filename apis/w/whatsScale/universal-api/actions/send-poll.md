# WhatsScale: Send Poll

Sends a poll message through WhatsScale.

```
POST https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/send-poll
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhatsScale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/send-poll" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatId": "string",
  "options[]": [
    "string"
  ],
  "question": "string",
  "session": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/send-poll', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chatId": "string",
    "options[]": ["string"],
    "question": "string",
    "session": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chatId` | string | yes | Recipient chat ID. |
| `multipleAnswers` | boolean | no | Allow respondents to select multiple poll options. |
| `options[]` | array<string> | yes | Array of 2-12 unique poll options. Accepts multiple values as an array. |
| `question` | string | yes | Poll question. |
| `session` | string | yes | Session name from /api/sessions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "timestamp": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `timestamp` | number |  |

## Native endpoint

Through the native WhatsScale API, this operation is `POST /api/sendPoll` (base URL `https://proxy.whatsscale.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-poll.md) for the provider-specific parameters and requirements.

