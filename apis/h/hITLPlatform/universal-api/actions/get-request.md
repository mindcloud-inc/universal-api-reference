# HITL Platform: Get Request



```
GET https://connect.mindcloud.co/v1/universal/hITLPlatform/latest/actions/get-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HITL Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hITLPlatform/latest/actions/get-request?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hITLPlatform/latest/actions/get-request?${params}`, {
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
| `id` | string | yes | The unique identifier of the request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "request": {
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `request.api_key_id` | string |  |
| `request.assignee_role` | string |  |
| `request.broadcasted_at` | date |  |
| `request.broadcasted_to[].email` | string |  |
| `request.broadcasted_to[].notification_error` | string |  |
| `request.broadcasted_to[].notification_sent` | boolean |  |
| `request.broadcasted_to[].role` | string |  |
| `request.broadcasted_to[].user_id` | string |  |
| `request.created_at` | date |  |
| `request.creator_id` | string |  |
| `request.default_response` | string |  |
| `request.id` | string |  |
| `request.loop_id` | string |  |
| `request.platform` | string |  |
| `request.priority` | string |  |
| `request.processing_type` | string |  |
| `request.request_text` | string |  |
| `request.response_type` | string |  |
| `request.status` | string |  |
| `request.timeout_at` | date |  |
| `request.type` | string |  |
| `request.updated_at` | date |  |
| `request.user_agent` | string |  |

## Native endpoint

Through the native HITL Platform API, this operation is `GET /api/requests/:id` (base URL `https://api.hitl.sh/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-request.md) for the provider-specific parameters and requirements.

