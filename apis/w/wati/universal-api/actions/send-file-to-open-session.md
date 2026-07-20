# Wati: Send File to Open Session

Sends a file in an open Wati session.

```
POST https://connect.mindcloud.co/v1/universal/wati/latest/actions/send-file-to-open-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wati `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wati/latest/actions/send-file-to-open-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "whatsappNumber": "string",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wati/latest/actions/send-file-to-open-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "whatsappNumber": "string",
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `whatsappNumber` | string | yes | WhatsApp phone number for the open session conversation. |
| `file` | file | yes | File to send in the active session. |
| `caption` | string | no | Optional caption for the file message. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "result": true,
      "ticketStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider message for the current ticket state. |
| `result` | boolean | Whether Wati accepted the file send request. |
| `ticketStatus` | string | Conversation ticket status returned by Wati. |

## Native endpoint

Through the native Wati API, this operation is `POST /api/v1/sendSessionFile/:whatsappNumber` (base URL `{{credentials.apiEndpointUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-file-to-open-session.md) for the provider-specific parameters and requirements.

