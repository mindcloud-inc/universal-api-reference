# Cloro: Get Async Status



```
GET https://connect.mindcloud.co/v1/universal/cloro/latest/actions/get-async-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloro/latest/actions/get-async-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloro/latest/actions/get-async-status?${params}`, {
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
      "concurrency": {
        "max": 1,
        "used": 1
      },
      "processingTasks": 1,
      "queuedTasks": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `concurrency.max` | number |  |
| `concurrency.used` | number |  |
| `processingTasks` | number |  |
| `queuedTasks` | number |  |

## Native endpoint

Through the native Cloro API, this operation is `GET /v1/async/status` (base URL `https://api.cloro.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-async-status.md) for the provider-specific parameters and requirements.

