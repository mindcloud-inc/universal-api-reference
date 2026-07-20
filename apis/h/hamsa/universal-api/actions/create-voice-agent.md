# Hamsa: Create Voice Agent

Creates a new voice agent in Hamsa.

```
POST https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/create-voice-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hamsa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/create-voice-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/create-voice-agent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agenticRag` | boolean | no |  |
| `agentName` | string | yes |  |
| `alignment` | object | no |  |
| `backgroundNoise` | boolean | no |  |
| `cancelNoisePer` | string | no |  |
| `description` | string | no |  |
| `enableAutoGainControl` | boolean | no |  |
| `greetingMessage` | string | no |  |
| `greetingMessageType` | string | no |  |
| `interrupt` | boolean | no |  |
| `knowledgeBaseItemsIds[]` | array<string> | no |  |
| `lang` | string | no |  |
| `languageDialectSwitcher` | boolean | no |  |
| `llmConfig` | object | no |  |
| `maxCallDuration` | number | no |  |
| `minInterruptionDuration` | number | no |  |
| `noiseCancellation` | string | no |  |
| `outcome` | string | no |  |
| `outcomeResponseShape` | object | no |  |
| `params` | object | no |  |
| `pokeMessages[]` | array<string> | no |  |
| `preamble` | string | no |  |
| `realTime` | boolean | no |  |
| `responseDelay` | number | no |  |
| `sendDenoisedToStt` | boolean | no |  |
| `silenceThreshold` | number | no |  |
| `speakerIdentification` | boolean | no |  |
| `thinkingVoice` | boolean | no |  |
| `tools` | object | no |  |
| `type` | string | no |  |
| `userInactivityTimeout` | number | no |  |
| `vadActivationThreshold` | number | no |  |
| `voiceDictionaryIds[]` | array<string> | no |  |
| `voiceId` | string | no |  |
| `waitForUserToSpeakFirst` | number | no |  |
| `webhookAuth` | object | no |  |
| `webhookUrl` | string | no |  |
| `webToolsIds[]` | array<string> | no |  |
| `webToolsOverrides` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agenticRag": true,
      "agentName": "Ava Chen",
      "alignment": {
        "greetingMessage": "string",
        "preamble": "string"
      },
      "apiKeyId": "string",
      "backgroundNoise": true,
      "cancelNoisePer": "string",
      "collectionId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "enableAutoGainControl": true,
      "greetingMessage": "string",
      "greetingMessageType": "string",
      "icon": "string",
      "id": "string",
      "interrupt": true,
      "isTemplate": true,
      "knowledgeBaseItemsIds": [
        [
          "string"
        ]
      ],
      "lang": "string",
      "languageDialectSwitcher": true,
      "llmConfig": {
        "apiKey": "string",
        "baseUrl": "https://example.com",
        "modelName": "Ava Chen",
        "provider": "string",
        "temperature": 1
      },
      "maxCallDuration": 1,
      "minInterruptionDuration": 1,
      "noiseCancellation": "string",
      "outcome": "string",
      "outcomeResponseShape": {
        "properties": {
          "test": {
            "description": "string",
            "type": 1
          }
        },
        "type": "string"
      },
      "pokeMessages": [
        [
          "string"
        ]
      ],
      "preamble": "string",
      "projectId": "string",
      "realTime": true,
      "responseDelay": 1,
      "sendDenoisedToStt": true,
      "silenceThreshold": 1,
      "speakerIdentification": true,
      "thinkingVoice": true,
      "tools": {
        "genderDetection": true,
        "smartCallEnd": true
      },
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userInactivityTimeout": 1,
      "vadActivationThreshold": 1,
      "voiceDictionaryIds": [
        [
          "string"
        ]
      ],
      "voiceId": "string",
      "voiceRecord": {
        "id": "string",
        "image": "string",
        "language": "string",
        "languageCode": "string",
        "name": "Ava Chen",
        "provider": "string"
      },
      "voiceRecordId": "string",
      "waitForUserToSpeakFirst": 1,
      "webhookAuth": {
        "authKey": "string",
        "authSecret": "string"
      },
      "webhookUrl": "https://example.com",
      "webToolsIds": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agenticRag` | boolean |  |
| `agentName` | string |  |
| `alignment.greetingMessage` | string |  |
| `alignment.preamble` | string |  |
| `apiKeyId` | string |  |
| `backgroundNoise` | boolean |  |
| `cancelNoisePer` | string |  |
| `collectionId` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `enableAutoGainControl` | boolean |  |
| `greetingMessage` | string |  |
| `greetingMessageType` | string |  |
| `icon` | string |  |
| `id` | string |  |
| `interrupt` | boolean |  |
| `isTemplate` | boolean |  |
| `knowledgeBaseItemsIds[]` | array<string> |  |
| `lang` | string |  |
| `languageDialectSwitcher` | boolean |  |
| `llmConfig.apiKey` | string |  |
| `llmConfig.baseUrl` | string |  |
| `llmConfig.modelName` | string |  |
| `llmConfig.provider` | string |  |
| `llmConfig.temperature` | number |  |
| `maxCallDuration` | number |  |
| `minInterruptionDuration` | number |  |
| `noiseCancellation` | string |  |
| `outcome` | string |  |
| `outcomeResponseShape.properties.test.description` | string |  |
| `outcomeResponseShape.properties.test.type` | number |  |
| `outcomeResponseShape.type` | string |  |
| `pokeMessages[]` | array<string> |  |
| `preamble` | string |  |
| `projectId` | string |  |
| `realTime` | boolean |  |
| `responseDelay` | number |  |
| `sendDenoisedToStt` | boolean |  |
| `silenceThreshold` | number |  |
| `speakerIdentification` | boolean |  |
| `thinkingVoice` | boolean |  |
| `tools.genderDetection` | boolean |  |
| `tools.smartCallEnd` | boolean |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `userInactivityTimeout` | number |  |
| `vadActivationThreshold` | number |  |
| `voiceDictionaryIds[]` | array<string> |  |
| `voiceId` | string |  |
| `voiceRecord.id` | string |  |
| `voiceRecord.image` | string |  |
| `voiceRecord.language` | string |  |
| `voiceRecord.languageCode` | string |  |
| `voiceRecord.name` | string |  |
| `voiceRecord.provider` | string |  |
| `voiceRecordId` | string |  |
| `waitForUserToSpeakFirst` | number |  |
| `webhookAuth.authKey` | string |  |
| `webhookAuth.authSecret` | string |  |
| `webhookUrl` | string |  |
| `webToolsIds[]` | array<string> |  |

## Native endpoint

Through the native Hamsa API, this operation is `POST /v1/voice-agents` (base URL `https://api.tryhamsa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-voice-agent.md) for the provider-specific parameters and requirements.

