# Dart: List Tasks

Retrieves tasks from Dart with optional filters.

```
GET https://connect.mindcloud.co/v1/universal/dart/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dart/latest/actions/list-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dart/latest/actions/list-tasks?${params}`, {
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
| `dartboardId` | string | no |  |
| `isCompleted` | string | no |  |
| `limit` | string | no |  |
| `offset` | string | no |  |
| `status` | string | no |  |
| `title` | string | no |  |
| `viewId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dartboard": "string",
      "htmlUrl": "https://example.com",
      "id": "string",
      "status": "string",
      "tags": [
        "string"
      ],
      "title": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `dartboard` | string |  |
| `htmlUrl` | string |  |
| `id` | string |  |
| `status` | string |  |
| `tags[]` | string |  |
| `title` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Dart API, this operation is `GET /tasks/list` (base URL `https://app.dartai.com/api/v0/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

