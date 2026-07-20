# LogMeIn: Send Session SMS Invitation

Sends a session SMS invitation from LogMeIn.

```
POST https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/send-session-sms-invitation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LogMeIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/send-session-sms-invitation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sessionId": "string",
  "language": "string",
  "phoneNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/send-session-sms-invitation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sessionId": "string",
    "language": "string",
    "phoneNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sessionId` | string | yes | Required session ID for the SMS invitation. |
| `language` | string | yes | Invitation language code such as EN, DE, ES, FR, HU, IT, PT, NL, JA, TW, CN, KR, or TH. |
| `phoneNumber` | string | yes | Phone number to send the session invitation to. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "phoneNumber": "string",
      "sessionId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `phoneNumber` | string |  |
| `sessionId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native LogMeIn API, this operation is `POST /goto-resolve/v1/sessions/:sessionId/invite/sms` (base URL `https://api.goto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-session-sms-invitation.md) for the provider-specific parameters and requirements.

