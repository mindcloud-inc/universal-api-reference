# Beatoven AI: Get Task Status

Retrieves composition task status from Beatoven AI.

```
GET https://connect.mindcloud.co/v1/universal/beatovenAI/latest/actions/get-task-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beatoven AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beatovenAI/latest/actions/get-task-status?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beatovenAI/latest/actions/get-task-status?${params}`, {
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
| `taskId` | string | yes | Beatoven composition task ID returned by a compose request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {
        "duration": 1,
        "prompt": {
          "text": "string"
        },
        "stems_url": {
          "bass": "https://example.com",
          "chords": "https://example.com",
          "melody": "https://example.com",
          "percussion": "https://example.com"
        },
        "track_id": "string",
        "track_url": "https://example.com"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta.duration` | number |  |
| `meta.prompt.text` | string |  |
| `meta.stems_url.bass` | string |  |
| `meta.stems_url.chords` | string |  |
| `meta.stems_url.melody` | string |  |
| `meta.stems_url.percussion` | string |  |
| `meta.track_id` | string |  |
| `meta.track_url` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Beatoven AI API, this operation is `GET /tasks/:taskId` (base URL `https://public-api.beatoven.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task-status.md) for the provider-specific parameters and requirements.

