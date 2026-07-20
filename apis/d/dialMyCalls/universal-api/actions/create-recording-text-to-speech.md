# DialMyCalls: Create Recording (Text-to-Speech)

Creates a text-to-speech recording in DialMyCalls.

```
POST https://connect.mindcloud.co/v1/universal/dialMyCalls/latest/actions/create-recording-text-to-speech
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DialMyCalls `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dialMyCalls/latest/actions/create-recording-text-to-speech" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "gender": "string",
  "language": "string",
  "name": "Ava Chen",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dialMyCalls/latest/actions/create-recording-text-to-speech', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "gender": "string",
    "language": "string",
    "name": "Ava Chen",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `gender` | string | yes | Gender of the recording. Options: M or F. |
| `language` | string | yes | Language of the recording. Options: en or es. |
| `name` | string | yes | The name of the recording. |
| `text` | string | yes | The text to convert to speech. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "processed": true,
      "seconds": 1,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
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
| `name` | string |  |
| `processed` | boolean |  |
| `seconds` | number |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native DialMyCalls API, this operation is `POST /recording/tts` (base URL `https://{{credentials.apiKey}}@api.dialmycalls.com/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-recording-text-to-speech.md) for the provider-specific parameters and requirements.

