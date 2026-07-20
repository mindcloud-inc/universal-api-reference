# LangChain: Create Feedback



```
POST https://connect.mindcloud.co/v1/universal/langChain/latest/actions/create-feedback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LangChain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/langChain/latest/actions/create-feedback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/langChain/latest/actions/create-feedback', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "comparative_experiment_id": "string",
      "correction": {},
      "created_at": "2026-05-07T12:00:00.000Z",
      "extra": {},
      "feedback_group_id": "string",
      "feedback_source": {},
      "feedback_thread_id": "string",
      "id": "string",
      "is_root": true,
      "key": "string",
      "modified_at": "2026-05-07T12:00:00.000Z",
      "run_id": "string",
      "score": 1,
      "session_id": "string",
      "start_time": "2026-05-07T12:00:00.000Z",
      "trace_id": "string",
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string | Optional feedback comment. |
| `comparative_experiment_id` | string | Optional comparative experiment UUID. |
| `correction` | object | Optional correction payload. |
| `created_at` | date | Creation timestamp. |
| `extra` | object | Additional provider metadata. |
| `feedback_group_id` | string | Optional feedback group UUID. |
| `feedback_source` | object | Feedback source metadata. |
| `feedback_thread_id` | string | Optional feedback thread UUID. |
| `id` | string | Feedback UUID. |
| `is_root` | boolean | Whether feedback is on a root run. |
| `key` | string | Feedback metric key. |
| `modified_at` | date | Last update timestamp. |
| `run_id` | string | Associated run UUID. |
| `score` | number | Numeric score. |
| `session_id` | string | Associated session UUID. |
| `start_time` | date | Associated run start time. |
| `trace_id` | string | Associated trace UUID. |
| `value` | object | Optional non-numeric value. |

## Native endpoint

Through the native LangChain API, this operation is `POST /api/v1/feedback` (base URL `https://api.smith.langchain.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-feedback.md) for the provider-specific parameters and requirements.

