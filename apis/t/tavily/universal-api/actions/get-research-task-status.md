# Tavily: Get Research Task Status

Retrieves Tavily research task status and results by request ID.

```
GET https://connect.mindcloud.co/v1/universal/tavily/latest/actions/get-research-task-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tavily `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tavily/latest/actions/get-research-task-status?connectionId=$CONNECTION_ID&requestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tavily/latest/actions/get-research-task-status?${params}`, {
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
| `requestId` | string | yes | The unique identifier of the research task. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "request_id": "string",
      "response_time": 1,
      "sources": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Research report content returned by Tavily. |
| `created_at` | date | Timestamp when the research task was created. |
| `request_id` | string | Unique request identifier for the research task. |
| `response_time` | number | Time in seconds it took to complete the request. |
| `sources` | array<object> | Sources used in the research report. |
| `status` | string | Current status of the research task. |

## Native endpoint

Through the native Tavily API, this operation is `GET /research/:request_id` (base URL `https://api.tavily.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-research-task-status.md) for the provider-specific parameters and requirements.

