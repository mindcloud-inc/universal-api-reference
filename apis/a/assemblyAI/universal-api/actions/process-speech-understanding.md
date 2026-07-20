# AssemblyAI: Process Speech Understanding

Creates speech understanding output from an AssemblyAI transcript.

```
POST https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/process-speech-understanding
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AssemblyAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/process-speech-understanding" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transcriptId": "string",
  "speechUnderstanding": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/process-speech-understanding', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transcriptId": "string",
    "speechUnderstanding": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transcriptId` | string | yes | The ID of the transcript to process. |
| `speechUnderstanding` | object | yes | Speech understanding task object with translation, speaker identification, and/or custom formatting request details. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "requestId": "string",
      "speechUnderstanding": {
        "request": {
          "translation": {
            "targetLanguages": [
              [
                "string"
              ]
            ]
          }
        },
        "response": {
          "translation": {
            "status": "string"
          }
        }
      },
      "translatedTexts": {
        "es": "string"
      },
      "utterances": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `requestId` | string |  |
| `speechUnderstanding` | object |  |
| `speechUnderstanding.request` | object |  |
| `speechUnderstanding.request.translation` | object |  |
| `speechUnderstanding.request.translation.targetLanguages[]` | array<string> |  |
| `speechUnderstanding.response` | object |  |
| `speechUnderstanding.response.translation` | object |  |
| `speechUnderstanding.response.translation.status` | string |  |
| `translatedTexts` | object |  |
| `translatedTexts.es` | string |  |
| `utterances` | object |  |

## Native endpoint

Through the native AssemblyAI API, this operation is `POST https://llm-gateway.assemblyai.com/v1/understanding` (base URL `https://api.assemblyai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/process-speech-understanding.md) for the provider-specific parameters and requirements.

