# Rev AI: Submit Transcription Job

Creates a new transcription job in Rev AI.

```
POST https://connect.mindcloud.co/v1/universal/revAI/latest/actions/submit-transcription-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rev AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/revAI/latest/actions/submit-transcription-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceConfig.url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/revAI/latest/actions/submit-transcription-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceConfig.url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceConfig.url` | string | yes | Publicly accessible media URL to transcribe. |
| `metadata` | string | no |  |
| `transcriber` | string | no | Examples from docs: machine, low_cost, fusion, human. |
| `language` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completed_on": "string",
      "created_on": "string",
      "duration_seconds": 1,
      "id": "string",
      "language": "string",
      "metadata": "string",
      "name": "Ava Chen",
      "status": "string",
      "strict_custom_vocabulary": true,
      "transcriber": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completed_on` | string |  |
| `created_on` | string |  |
| `duration_seconds` | number |  |
| `id` | string |  |
| `language` | string |  |
| `metadata` | string |  |
| `name` | string |  |
| `status` | string |  |
| `strict_custom_vocabulary` | boolean |  |
| `transcriber` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Rev AI API, this operation is `POST /speechtotext/v1/jobs` (base URL `https://api.rev.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-transcription-job.md) for the provider-specific parameters and requirements.

