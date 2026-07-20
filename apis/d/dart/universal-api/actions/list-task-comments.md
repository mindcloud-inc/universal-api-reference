# Dart: List Task Comments

Retrieves task comments from Dart with pagination.

```
GET https://connect.mindcloud.co/v1/universal/dart/latest/actions/list-task-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dart/latest/actions/list-task-comments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dart/latest/actions/list-task-comments?${params}`, {
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
| `limit` | string | no |  |
| `offset` | string | no |  |
| `taskId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "htmlUrl": "https://example.com",
      "id": "string",
      "taskId": "string",
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `htmlUrl` | string |  |
| `id` | string |  |
| `taskId` | string |  |
| `text` | string |  |

## Native endpoint

Through the native Dart API, this operation is `GET /comments/list` (base URL `https://app.dartai.com/api/v0/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-task-comments.md) for the provider-specific parameters and requirements.

