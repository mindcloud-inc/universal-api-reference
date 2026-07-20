# CRM Messaging: Make Voice Call

Starts a voice call in CRM Messaging.

```
POST https://connect.mindcloud.co/v1/universal/cRMMessaging/latest/actions/make-voice-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CRM Messaging `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cRMMessaging/latest/actions/make-voice-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "toNumber": "string",
  "fromNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cRMMessaging/latest/actions/make-voice-call', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "toNumber": "string",
    "fromNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `toNumber` | string | yes |  |
| `fromNumber` | string | yes |  |
| `content` | string | no |  |
| `messageType` | string | no | Default: `text`. |
| `voice` | string | no | Default: `Polly.Joanna`. |
| `audioUrl` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callId": "string",
      "callStatus": "string",
      "fromNumber": "string",
      "messageId": "string",
      "status": "string",
      "toNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callId` | string |  |
| `callStatus` | string |  |
| `fromNumber` | string |  |
| `messageId` | string |  |
| `status` | string |  |
| `toNumber` | string |  |

## Native endpoint

Through the native CRM Messaging API, this operation is `POST https://campaigns.crm-messaging.cloud/api/voice-call` (base URL `https://app.crm-messaging.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/make-voice-call.md) for the provider-specific parameters and requirements.

