# Langfuse: Get Trace

Retrieves a trace from Langfuse.

```
GET https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/get-trace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langfuse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/get-trace?connectionId=$CONNECTION_ID&traceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "traceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/get-trace?${params}`, {
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
| `fields` | string | no |  |
| `traceId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "environment": "string",
      "id": "string",
      "input": "string",
      "metadata": "string",
      "name": "Ava Chen",
      "output": "string",
      "public": true,
      "release": "string",
      "sessionId": "string",
      "tags": [
        "string"
      ],
      "timestamp": "2026-05-07T12:00:00.000Z",
      "userId": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `environment` | string |  |
| `id` | string |  |
| `input` | string |  |
| `metadata` | string |  |
| `name` | string |  |
| `output` | string |  |
| `public` | boolean |  |
| `release` | string |  |
| `sessionId` | string |  |
| `tags` | array<string> |  |
| `timestamp` | date |  |
| `userId` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Langfuse API, this operation is `GET /traces/:traceId` (base URL `https://cloud.langfuse.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-trace.md) for the provider-specific parameters and requirements.

