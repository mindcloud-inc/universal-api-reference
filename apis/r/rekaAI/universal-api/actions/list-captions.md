# Reka AI: List Captions

Retrieves captions from a Reka AI video.

```
GET https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/list-captions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reka AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/list-captions?connectionId=$CONNECTION_ID&video_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "video_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/list-captions?${params}`, {
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
| `video_id` | string | yes | The video identifier whose captions to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "message": "string",
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
| `message` | string | Human-readable message. |
| `status` | string | Current status. |

## Native endpoint

Through the native Reka AI API, this operation is `GET https://vision-agent.api.reka.ai/v2/videos/:video_id/captions` (base URL `https://api.reka.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-captions.md) for the provider-specific parameters and requirements.

