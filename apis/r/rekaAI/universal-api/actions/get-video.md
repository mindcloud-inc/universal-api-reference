# Reka AI: Get Video

Retrieves a video from Reka AI.

```
GET https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/get-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reka AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/get-video?connectionId=$CONNECTION_ID&video_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "video_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/get-video?${params}`, {
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
| `video_id` | string | yes | The video identifier to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Primary identifier. |
| `name` | string | Display name. |
| `status` | string | Status value. |

## Native endpoint

Through the native Reka AI API, this operation is `GET https://vision-agent.api.reka.ai/v2/videos/:video_id` (base URL `https://api.reka.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video.md) for the provider-specific parameters and requirements.

