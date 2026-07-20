# FutureAGI: List Eval Tasks



```
GET https://connect.mindcloud.co/v1/universal/futureAGI/latest/actions/list-eval-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FutureAGI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/futureAGI/latest/actions/list-eval-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/futureAGI/latest/actions/list-eval-tasks?${params}`, {
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
      "result": {
        "config": [
          {}
        ],
        "metadata": {
          "totalRows": 1
        },
        "table": [
          {}
        ]
      },
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result.config` | array<object> |  |
| `result.metadata.totalRows` | number |  |
| `result.table` | array<object> |  |
| `status` | boolean |  |

## Native endpoint

Through the native FutureAGI API, this operation is `GET /tracer/eval-task/list_eval_tasks/` (base URL `https://api.futureagi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-eval-tasks.md) for the provider-specific parameters and requirements.

