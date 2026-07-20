# D7 Networks: Send SMS

Sends an SMS message with D7 Networks.

```
POST https://connect.mindcloud.co/v1/universal/d7Networks/latest/actions/send-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a D7 Networks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/d7Networks/latest/actions/send-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messages[].recipients[]": [
    "string"
  ],
  "messages[].content": "string",
  "message_globals.originator": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/d7Networks/latest/actions/send-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messages[].recipients[]": ["string"],
    "messages[].content": "string",
    "message_globals.originator": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messages[].recipients[]` | array<string> | yes | Mobile numbers with country codes to receive the SMS. |
| `messages[].content` | string | yes | Text message content. |
| `message_globals.originator` | string | yes | Sender ID or brand name shown to the recipient. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `message_globals.report_url` | string | no | Optional delivery report webhook URL. |
| `message_globals.tag` | string | no | Optional client reference tag for the message. |

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
| `created_at` | date | Request creation time. |
| `request_id` | string | D7 request identifier. |
| `status` | string | Request status. |

## Native endpoint

Through the native D7 Networks API, this operation is `POST /messages/v1/send` (base URL `https://api.d7networks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-sms.md) for the provider-specific parameters and requirements.

