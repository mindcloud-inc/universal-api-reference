# HITL Platform: List Requests



```
GET https://connect.mindcloud.co/v1/universal/hITLPlatform/latest/actions/list-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HITL Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hITLPlatform/latest/actions/list-requests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hITLPlatform/latest/actions/list-requests?${params}`, {
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
      "count": 1,
      "requests": [
        {
          "api_key_id": "string",
          "assignee_role": "string",
          "broadcasted_at": "2026-05-07T12:00:00.000Z",
          "broadcasted_to": [
            {
              "email": "ava@example.com",
              "notification_error": "string",
              "notification_sent": true,
              "role": "string",
              "user_id": "string"
            }
          ],
          "created_at": "2026-05-07T12:00:00.000Z",
          "creator_id": "string",
          "default_response": "string",
          "id": "string",
          "loop_id": "string",
          "platform": "string",
          "priority": "string",
          "processing_type": "string",
          "request_text": "string",
          "response_type": "string",
          "status": "string",
          "timeout_at": "2026-05-07T12:00:00.000Z",
          "type": "string",
          "updated_at": "2026-05-07T12:00:00.000Z",
          "user_agent": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `requests[].api_key_id` | string |  |
| `requests[].assignee_role` | string |  |
| `requests[].broadcasted_at` | date |  |
| `requests[].broadcasted_to[].email` | string |  |
| `requests[].broadcasted_to[].notification_error` | string |  |
| `requests[].broadcasted_to[].notification_sent` | boolean |  |
| `requests[].broadcasted_to[].role` | string |  |
| `requests[].broadcasted_to[].user_id` | string |  |
| `requests[].created_at` | date |  |
| `requests[].creator_id` | string |  |
| `requests[].default_response` | string |  |
| `requests[].id` | string |  |
| `requests[].loop_id` | string |  |
| `requests[].platform` | string |  |
| `requests[].priority` | string |  |
| `requests[].processing_type` | string |  |
| `requests[].request_text` | string |  |
| `requests[].response_type` | string |  |
| `requests[].status` | string |  |
| `requests[].timeout_at` | date |  |
| `requests[].type` | string |  |
| `requests[].updated_at` | date |  |
| `requests[].user_agent` | string |  |

## Native endpoint

Through the native HITL Platform API, this operation is `GET /api/requests` (base URL `https://api.hitl.sh/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-requests.md) for the provider-specific parameters and requirements.

