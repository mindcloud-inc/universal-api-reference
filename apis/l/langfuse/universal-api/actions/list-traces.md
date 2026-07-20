# Langfuse: List Traces

Retrieves traces from Langfuse.

```
GET https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/list-traces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langfuse `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/list-traces?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/list-traces?${params}`, {
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
| `environment` | string | no |  |
| `fields` | string | no |  |
| `filter` | string | no |  |
| `fromTimestamp` | string | no |  |
| `name` | string | no |  |
| `orderBy` | string | no |  |
| `release` | string | no |  |
| `sessionId` | string | no |  |
| `tags` | string | no |  |
| `toTimestamp` | string | no |  |
| `userId` | string | no |  |
| `version` | string | no |  |

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

Through the native Langfuse API, this operation is `GET /traces` (base URL `https://cloud.langfuse.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-traces.md) for the provider-specific parameters and requirements.

