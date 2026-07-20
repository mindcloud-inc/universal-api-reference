# Rev AI: List Transcription Jobs

Retrieves transcription jobs from Rev AI.

```
GET https://connect.mindcloud.co/v1/universal/revAI/latest/actions/list-transcription-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rev AI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/revAI/latest/actions/list-transcription-jobs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/revAI/latest/actions/list-transcription-jobs?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no |  |
| `startingAfter` | string | no |  |

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

Through the native Rev AI API, this operation is `GET /speechtotext/v1/jobs` (base URL `https://api.rev.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-transcription-jobs.md) for the provider-specific parameters and requirements.

