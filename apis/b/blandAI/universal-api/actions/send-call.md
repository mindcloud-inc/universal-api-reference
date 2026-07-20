# Bland AI: Send Call

Creates a new call in Bland AI.

```
POST https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/send-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bland AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/send-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "phoneNumber": "string",
  "task": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/send-call', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "phoneNumber": "string",
    "task": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `phoneNumber` | string | yes |  |
| `voice` | string | no |  |
| `pathwayId` | string | no |  |
| `pathwayVersion` | number | no |  |
| `task` | string | yes |  |
| `firstSentence` | string | no |  |
| `personaId` | string | no |  |
| `model` | string | no |  |
| `language` | string | no |  |
| `waitForGreeting` | boolean | no |  |
| `pronunciationGuide[]` | array<string> | no |  |
| `temperature` | number | no |  |
| `interruptionThreshold` | number | no |  |
| `from` | string | no |  |
| `dialingStrategy` | object | no |  |
| `timezone` | string | no |  |
| `startTime` | string | no |  |
| `transferPhoneNumber` | string | no |  |
| `transferList` | object | no |  |
| `maxDuration` | number | no |  |
| `tools[]` | array<string> | no |  |
| `backgroundTrack` | string | no |  |
| `noiseCancellation` | boolean | no |  |
| `blockInterruptions` | boolean | no |  |
| `record` | boolean | no |  |
| `voicemail` | object | no |  |
| `citationSchemaIds[]` | array<string> | no |  |
| `summaryPrompt` | string | no |  |
| `retry` | object | no |  |
| `dispositions[]` | array<string> | no |  |
| `requestData` | object | no |  |
| `metadata` | object | no |  |
| `webhook` | string | no |  |
| `webhookEvents[]` | array<string> | no |  |
| `dynamicData[]` | array<object> | no |  |
| `keywords[]` | array<string> | no |  |
| `ignoreButtonPress` | boolean | no |  |
| `precallDtmfSequence` | string | no |  |
| `guardRails[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batch_id": "string",
      "call_id": "string",
      "errors": [
        "string"
      ],
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batch_id` | string |  |
| `call_id` | string |  |
| `errors` | array |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Bland AI API, this operation is `POST /v1/calls` (base URL `https://api.bland.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-call.md) for the provider-specific parameters and requirements.

