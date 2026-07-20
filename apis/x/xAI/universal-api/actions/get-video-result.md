# xAI: Get Video Result

Retrieves a video result from the xAI API.

```
GET https://connect.mindcloud.co/v1/universal/xAI/latest/actions/get-video-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xAI/latest/actions/get-video-result?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xAI/latest/actions/get-video-result?${params}`, {
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
| `request_id` | string | no | Deferred video request ID returned by a video generation or edit request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": {},
      "model": "string",
      "progress": 1,
      "status": "string",
      "video": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | object |  |
| `model` | string |  |
| `progress` | number |  |
| `status` | string |  |
| `video` | object |  |

## Native endpoint

Through the native xAI API, this operation is `GET /videos/:request_id` (base URL `https://api.x.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video-result.md) for the provider-specific parameters and requirements.

