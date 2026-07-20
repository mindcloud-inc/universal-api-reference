# Rev AI: Submit Topic Extraction Job

Creates a topic extraction job in Rev AI.

```
POST https://connect.mindcloud.co/v1/universal/revAI/latest/actions/submit-topic-extraction-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rev AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/revAI/latest/actions/submit-topic-extraction-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/revAI/latest/actions/submit-topic-extraction-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `text` | string | yes |  |
| `metadata` | string | no |  |
| `language` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completed_on": "string",
      "created_on": "string",
      "id": "string",
      "metadata": "string",
      "status": "string",
      "type": "string",
      "word_count": 1
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
| `id` | string |  |
| `metadata` | string |  |
| `status` | string |  |
| `type` | string |  |
| `word_count` | number |  |

## Native endpoint

Through the native Rev AI API, this operation is `POST /topic_extraction/v1/jobs` (base URL `https://api.rev.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-topic-extraction-job.md) for the provider-specific parameters and requirements.

