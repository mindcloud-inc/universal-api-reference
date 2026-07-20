# D7 Networks: Send Viber Message

Sends a Viber message with D7 Networks.

```
POST https://connect.mindcloud.co/v1/universal/d7Networks/latest/actions/send-viber-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a D7 Networks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/d7Networks/latest/actions/send-viber-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messages[].originator": "string",
  "messages[].recipients[]": [
    "string"
  ],
  "messages[].content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/d7Networks/latest/actions/send-viber-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messages[].originator": "string",
    "messages[].recipients[]": ["string"],
    "messages[].content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messages[].originator` | string | yes | Approved Viber sender/originator. |
| `messages[].recipients[]` | array<string> | yes | Recipient phone numbers with country codes. |
| `messages[].content` | string | yes | Viber message text. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `message_globals.report_url` | string | no | Optional delivery report webhook URL. |
| `message_globals.tag` | string | no | Optional client reference tag. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "request_id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `request_id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native D7 Networks API, this operation is `POST /viber/v1/send` (base URL `https://api.d7networks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-viber-message.md) for the provider-specific parameters and requirements.

