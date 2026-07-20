# Minimax: Query Video Template Generation Task

Retrieves a video agent task status from Minimax.

```
GET https://connect.mindcloud.co/v1/universal/minimax/latest/actions/query-video-template-generation-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Minimax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/minimax/latest/actions/query-video-template-generation-task?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/minimax/latest/actions/query-video-template-generation-task?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "base_resp": {
        "status_code": 1,
        "status_msg": "string"
      },
      "status": "string",
      "task_id": "string",
      "video_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `base_resp` | object |  |
| `base_resp.status_code` | number |  |
| `base_resp.status_msg` | string |  |
| `status` | string |  |
| `task_id` | string |  |
| `video_url` | string |  |

## Native endpoint

Through the native Minimax API, this operation is `GET /v1/query/video_template_generation` (base URL `https://api.minimax.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-video-template-generation-task.md) for the provider-specific parameters and requirements.

