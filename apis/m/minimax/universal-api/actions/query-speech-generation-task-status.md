# Minimax: Query Speech Generation Task Status

Retrieves a speech generation task status from Minimax.

```
GET https://connect.mindcloud.co/v1/universal/minimax/latest/actions/query-speech-generation-task-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Minimax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/minimax/latest/actions/query-speech-generation-task-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/minimax/latest/actions/query-speech-generation-task-status?${params}`, {
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
      "file_id": 1,
      "status": "string",
      "task_id": 1
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
| `file_id` | number |  |
| `status` | string |  |
| `task_id` | number |  |

## Native endpoint

Through the native Minimax API, this operation is `GET /v1/query/t2a_async_query_v2` (base URL `https://api.minimax.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-speech-generation-task-status.md) for the provider-specific parameters and requirements.

