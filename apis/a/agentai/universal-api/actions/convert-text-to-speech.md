# Agent.ai: Convert Text To Speech

Creates a speech audio file from text in Agent.ai.

```
POST https://connect.mindcloud.co/v1/universal/agentai/latest/actions/convert-text-to-speech
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/agentai/latest/actions/convert-text-to-speech" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "textToSpeech": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agentai/latest/actions/convert-text-to-speech', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "textToSpeech": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `textToSpeech` | string | yes | Text to convert to speech. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Generated audio file URL. |
| `status` | number | HTTP status code of the action response. |

## Native endpoint

Through the native Agent.ai API, this operation is `POST /action/output_audio` (base URL `https://api-lr.agent.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-text-to-speech.md) for the provider-specific parameters and requirements.

