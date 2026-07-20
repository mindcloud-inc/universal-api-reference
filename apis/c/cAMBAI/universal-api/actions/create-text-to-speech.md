# CAMB.AI: Create Text-to-Speech

Creates a new text-to-speech task in CAMB.AI.

```
POST https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/create-text-to-speech
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CAMB.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/create-text-to-speech" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "text": "string",
  "voiceId": 1,
  "languageId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/create-text-to-speech', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "text": "string",
    "voiceId": 1,
    "languageId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `text` | string | yes | Text to convert into speech. |
| `voiceId` | number | yes | Voice identifier from List Voices. |
| `languageId` | number | yes | Source language identifier for the speech. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "task_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `task_id` | string | Task identifier for the text-to-speech generation request. |

## Native endpoint

Through the native CAMB.AI API, this operation is `POST /tts` (base URL `https://client.camb.ai/apis`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-text-to-speech.md) for the provider-specific parameters and requirements.

