# Hamsa: Update Voice Agent

Updates an existing voice agent in Hamsa.

```
PUT https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/update-voice-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hamsa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/update-voice-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "voiceAgentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/update-voice-agent', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "voiceAgentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callSettings` | object | no |  |
| `conversation` | object | no |  |
| `knowledgeBaseItemsIds[]` | array<string> | no |  |
| `llm` | object | no |  |
| `name` | string | no |  |
| `outcomeResponseShape` | object | no |  |
| `phoneNumber` | object | no |  |
| `tools[]` | array<object> | no |  |
| `type` | string | no |  |
| `voice` | object | no |  |
| `voiceAgentId` | string | yes |  |
| `voiceDictionaryIds[]` | array<string> | no |  |
| `webhookAuth` | object | no |  |
| `webhookUrl` | string | no |  |
| `workflow` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": {
        "plan": "string"
      },
      "callSettings": {
        "agenticRag": true,
        "backgroundNoise": true,
        "cancelNoisePer": "string",
        "enableAutoGainControl": true,
        "genderDetection": true,
        "interrupt": true,
        "languageDialectSwitcher": true,
        "maxCallDuration": 1,
        "minInterruptionDuration": 1,
        "noiseCancellation": "string",
        "responseDelay": 1,
        "sendDenoisedToStt": true,
        "silenceThreshold": 1,
        "smartCallEnd": true,
        "speakerIdentification": true,
        "thinkingVoice": true,
        "userInactivityTimeout": 1,
        "vadActivationThreshold": 1
      },
      "conversation": {
        "alignment": {
          "greetingMessage": "string",
          "preamble": "string"
        },
        "greetingMessage": "string",
        "greetingMessageType": "string",
        "params": {},
        "pokeMessages": [
          [
            "string"
          ]
        ],
        "preamble": "string"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "knowledgeBaseItemsIds": [
        [
          "string"
        ]
      ],
      "llm": {
        "apiKey": "string",
        "baseUrl": "https://example.com",
        "model": "string",
        "provider": "string",
        "temperature": 1
      },
      "name": "Ava Chen",
      "outcomeResponseShape": {
        "properties": {
          "test": {
            "description": "string",
            "type": 1
          }
        },
        "type": "string"
      },
      "phoneNumber": {
        "id": "string",
        "type": "string"
      },
      "resolvedWebTools": [
        [
          {}
        ]
      ],
      "tools": [
        [
          {}
        ]
      ],
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "voice": {
        "lang": "string",
        "voiceId": "string",
        "voiceRecord": {
          "id": "string",
          "image": "string",
          "language": "string",
          "languageCode": "string",
          "name": "Ava Chen",
          "provider": "string"
        },
        "voiceRecordId": "string"
      },
      "voiceDictionaryIds": [
        [
          "string"
        ]
      ],
      "webhookAuth": {
        "authKey": "string",
        "authSecret": "string"
      },
      "webhookUrl": "https://example.com",
      "workflow": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account.plan` | string |  |
| `callSettings.agenticRag` | boolean |  |
| `callSettings.backgroundNoise` | boolean |  |
| `callSettings.cancelNoisePer` | string |  |
| `callSettings.enableAutoGainControl` | boolean |  |
| `callSettings.genderDetection` | boolean |  |
| `callSettings.interrupt` | boolean |  |
| `callSettings.languageDialectSwitcher` | boolean |  |
| `callSettings.maxCallDuration` | number |  |
| `callSettings.minInterruptionDuration` | number |  |
| `callSettings.noiseCancellation` | string |  |
| `callSettings.responseDelay` | number |  |
| `callSettings.sendDenoisedToStt` | boolean |  |
| `callSettings.silenceThreshold` | number |  |
| `callSettings.smartCallEnd` | boolean |  |
| `callSettings.speakerIdentification` | boolean |  |
| `callSettings.thinkingVoice` | boolean |  |
| `callSettings.userInactivityTimeout` | number |  |
| `callSettings.vadActivationThreshold` | number |  |
| `conversation.alignment.greetingMessage` | string |  |
| `conversation.alignment.preamble` | string |  |
| `conversation.greetingMessage` | string |  |
| `conversation.greetingMessageType` | string |  |
| `conversation.params` | object |  |
| `conversation.pokeMessages[]` | array<string> |  |
| `conversation.preamble` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `knowledgeBaseItemsIds[]` | array<string> |  |
| `llm.apiKey` | string |  |
| `llm.baseUrl` | string |  |
| `llm.model` | string |  |
| `llm.provider` | string |  |
| `llm.temperature` | number |  |
| `name` | string |  |
| `outcomeResponseShape.properties.test.description` | string |  |
| `outcomeResponseShape.properties.test.type` | number |  |
| `outcomeResponseShape.type` | string |  |
| `phoneNumber.id` | string |  |
| `phoneNumber.type` | string |  |
| `resolvedWebTools[]` | array<object> |  |
| `tools[]` | array<object> |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `voice.lang` | string |  |
| `voice.voiceId` | string |  |
| `voice.voiceRecord.id` | string |  |
| `voice.voiceRecord.image` | string |  |
| `voice.voiceRecord.language` | string |  |
| `voice.voiceRecord.languageCode` | string |  |
| `voice.voiceRecord.name` | string |  |
| `voice.voiceRecord.provider` | string |  |
| `voice.voiceRecordId` | string |  |
| `voiceDictionaryIds[]` | array<string> |  |
| `webhookAuth.authKey` | string |  |
| `webhookAuth.authSecret` | string |  |
| `webhookUrl` | string |  |
| `workflow` | object |  |

## Native endpoint

Through the native Hamsa API, this operation is `PATCH /v2/voice-agents/:voiceAgentId` (base URL `https://api.tryhamsa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-voice-agent.md) for the provider-specific parameters and requirements.

