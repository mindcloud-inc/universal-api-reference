# ZapCap: Get Video Task

Retrieves a video task from ZapCap.

```
GET https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/get-video-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ZapCap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/get-video-task?connectionId=$CONNECTION_ID&video=string&task=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "video": "string",
  "task": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/get-video-task?${params}`, {
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
| `video` | string | yes | ZapCap video ID. |
| `task` | string | yes | ZapCap task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "downloadUrl": "https://example.com",
      "error": "string",
      "id": "string",
      "language": "string",
      "status": "string",
      "transcript": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `downloadUrl` | string | Rendered video download URL when available. |
| `error` | string | Provider error summary when present. |
| `id` | string | ZapCap task ID. |
| `language` | string | Detected or requested language when present. |
| `status` | string | Current task lifecycle status. |
| `transcript` | string | Transcript download URL when available. |

## Native endpoint

Through the native ZapCap API, this operation is `GET /videos/:videoId/task/:id` (base URL `https://api.zapcap.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video-task.md) for the provider-specific parameters and requirements.

