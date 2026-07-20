# HITL Platform: Create Request



```
POST https://connect.mindcloud.co/v1/universal/hITLPlatform/latest/actions/create-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HITL Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hITLPlatform/latest/actions/create-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "loopId": "string",
  "platform": "api",
  "priority": "string",
  "processingType": "string",
  "requestText": "string",
  "responseType": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hITLPlatform/latest/actions/create-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "loopId": "string",
    "platform": "api",
    "priority": "string",
    "processingType": "string",
    "requestText": "string",
    "responseType": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callbackUrl` | string | no | Webhook URL to notify when the request completes. |
| `defaultResponse` | string | no | Fallback response used if the request times out. |
| `imageUrl` | string | no | Image URL to review when the content type is image. |
| `loopId` | string | yes | The loop where the request will be created. |
| `platform` | string | yes | Source platform creating the request. Default: `api`. |
| `priority` | string | yes | Priority level such as low, medium, high, or critical. |
| `processingType` | string | yes | Processing urgency type such as time-sensitive or deferred. |
| `requestText` | string | yes | Main request content for the reviewer. |
| `responseType` | string | yes | Expected response type, such as text or single_select. |
| `timeoutSeconds` | number | no | Timeout in seconds for time-sensitive requests. |
| `type` | string | yes | Content type to review, such as markdown or image. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "broadcasted_to": 1,
      "notifications_sent": 1,
      "polling_url": "https://example.com",
      "priority": "string",
      "processing_type": "string",
      "request_id": "string",
      "status": "string",
      "timeout_at": "2026-05-07T12:00:00.000Z",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `broadcasted_to` | number |  |
| `notifications_sent` | number |  |
| `polling_url` | string |  |
| `priority` | string |  |
| `processing_type` | string |  |
| `request_id` | string |  |
| `status` | string |  |
| `timeout_at` | date |  |
| `type` | string |  |

## Native endpoint

Through the native HITL Platform API, this operation is `POST /api/loops/:loopId/requests` (base URL `https://api.hitl.sh/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-request.md) for the provider-specific parameters and requirements.

