# Gladia: Create Transcription

Creates a transcription job in Gladia.

```
POST https://connect.mindcloud.co/v1/universal/gladia/latest/actions/create-transcription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gladia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gladia/latest/actions/create-transcription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "audioUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gladia/latest/actions/create-transcription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "audioUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `audioUrl` | string | yes | Gladia file URL or external audio URL for the transcription job. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "resultUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `resultUrl` | string |  |

## Native endpoint

Through the native Gladia API, this operation is `POST /v2/transcription` (base URL `https://api.gladia.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transcription.md) for the provider-specific parameters and requirements.

