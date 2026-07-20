# Hamsa: Call Voice Agent via Twilio

Starts a Twilio call to a Hamsa voice agent.

```
POST https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/call-voice-agent-via-twilio
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hamsa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/call-voice-agent-via-twilio" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "toNumber": "string",
  "twilioPhoneNumber": "string",
  "voiceAgentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/call-voice-agent-via-twilio', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "toNumber": "string",
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
| `agentDetails` | object | no |  |
| `params` | object | no |  |
| `toNumber` | string | yes |  |
| `twilioPhoneNumber` | string | yes |  |
| `voiceAgentId` | string | yes |  |
| `webhookAuth` | object | no |  |
| `webhookUrl` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiKeyId": "string",
      "billingId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "jobResponse": {
        "agentDetails": {
          "agentName": "Ava Chen",
          "apiKeyId": "string",
          "description": "string",
          "greetingMessage": "string",
          "id": "string",
          "interrupt": true,
          "lang": "string",
          "outcome": "string",
          "preamble": "string",
          "projectId": "string",
          "realTime": true,
          "silenceThreshold": 1,
          "tools": {
            "accessToken": "string",
            "calendarId": "string",
            "calendarName": "Ava Chen",
            "eventTitle": "string",
            "meetingDuration": 1,
            "refreshToken": "string",
            "timezone": "string",
            "voiceAgentToolsId": "string"
          },
          "voiceRecord": {
            "id": "string",
            "language": "string",
            "name": "Ava Chen",
            "provider": "string"
          },
          "voiceRecordId": "string"
        },
        "callParams": {
          "machineNumber": "string",
          "userNumber": "string"
        },
        "text": "string",
        "ttsMediaFile": "string"
      },
      "mediaUrl": "https://example.com",
      "model": "string",
      "processingType": "string",
      "relevantJobId": "string",
      "status": "string",
      "systemModelKey": "string",
      "title": "string",
      "totalCost": 1,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "usageTime": "string",
      "voiceAgentId": "string",
      "webhookUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiKeyId` | string |  |
| `billingId` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `jobResponse.agentDetails.agentName` | string |  |
| `jobResponse.agentDetails.apiKeyId` | string |  |
| `jobResponse.agentDetails.description` | string |  |
| `jobResponse.agentDetails.greetingMessage` | string |  |
| `jobResponse.agentDetails.id` | string |  |
| `jobResponse.agentDetails.interrupt` | boolean |  |
| `jobResponse.agentDetails.lang` | string |  |
| `jobResponse.agentDetails.outcome` | string |  |
| `jobResponse.agentDetails.preamble` | string |  |
| `jobResponse.agentDetails.projectId` | string |  |
| `jobResponse.agentDetails.realTime` | boolean |  |
| `jobResponse.agentDetails.silenceThreshold` | number |  |
| `jobResponse.agentDetails.tools.accessToken` | string |  |
| `jobResponse.agentDetails.tools.calendarId` | string |  |
| `jobResponse.agentDetails.tools.calendarName` | string |  |
| `jobResponse.agentDetails.tools.eventTitle` | string |  |
| `jobResponse.agentDetails.tools.meetingDuration` | number |  |
| `jobResponse.agentDetails.tools.refreshToken` | string |  |
| `jobResponse.agentDetails.tools.timezone` | string |  |
| `jobResponse.agentDetails.tools.voiceAgentToolsId` | string |  |
| `jobResponse.agentDetails.voiceRecord.id` | string |  |
| `jobResponse.agentDetails.voiceRecord.language` | string |  |
| `jobResponse.agentDetails.voiceRecord.name` | string |  |
| `jobResponse.agentDetails.voiceRecord.provider` | string |  |
| `jobResponse.agentDetails.voiceRecordId` | string |  |
| `jobResponse.callParams.machineNumber` | string |  |
| `jobResponse.callParams.userNumber` | string |  |
| `jobResponse.text` | string |  |
| `jobResponse.ttsMediaFile` | string |  |
| `mediaUrl` | string |  |
| `model` | string |  |
| `processingType` | string |  |
| `relevantJobId` | string |  |
| `status` | string |  |
| `systemModelKey` | string |  |
| `title` | string |  |
| `totalCost` | number |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `usageTime` | string |  |
| `voiceAgentId` | string |  |
| `webhookUrl` | string |  |

## Native endpoint

Through the native Hamsa API, this operation is `POST /v1/voice-agents/twilio/call` (base URL `https://api.tryhamsa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/call-voice-agent-via-twilio.md) for the provider-specific parameters and requirements.

