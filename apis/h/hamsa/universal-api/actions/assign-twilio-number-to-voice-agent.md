# Hamsa: Assign Twilio Number to Voice Agent

Assigns a Twilio number to a Hamsa voice agent.

```
POST https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/assign-twilio-number-to-voice-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hamsa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/assign-twilio-number-to-voice-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "twilioPhoneNumber": "string",
  "voiceAgentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/assign-twilio-number-to-voice-agent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "twilioPhoneNumber": "string",
    "voiceAgentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `twilioPhoneNumber` | string | yes |  |
| `voiceAgentId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isActive": true,
      "label": "string",
      "number": "string",
      "numberSid": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string",
      "voiceAgentId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | string |  |
| `isActive` | boolean |  |
| `label` | string |  |
| `number` | string |  |
| `numberSid` | string |  |
| `updatedAt` | date |  |
| `userId` | string |  |
| `voiceAgentId` | string |  |

## Native endpoint

Through the native Hamsa API, this operation is `POST /v1/voice-agents/twilio/assign-number` (base URL `https://api.tryhamsa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-twilio-number-to-voice-agent.md) for the provider-specific parameters and requirements.

