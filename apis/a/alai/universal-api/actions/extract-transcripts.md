# Alai: Extract Transcripts

Creates an async transcript extraction for an Alai presentation.

```
POST https://connect.mindcloud.co/v1/universal/alai/latest/actions/extract-transcripts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/alai/latest/actions/extract-transcripts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "presentationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/alai/latest/actions/extract-transcripts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "presentationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `presentationId` | string | yes | Presentation identifier to transcribe. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "generationId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `generationId` | string |  |

## Native endpoint

Through the native Alai API, this operation is `POST /presentations/:presentation_id/transcripts` (base URL `https://slides-api.getalai.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-transcripts.md) for the provider-specific parameters and requirements.

