# Galileo: List Log Streams

Finds log streams for a Galileo project.

```
GET https://connect.mindcloud.co/v1/universal/galileo/latest/actions/list-log-streams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Galileo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/galileo/latest/actions/list-log-streams?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/galileo/latest/actions/list-log-streams?${params}`, {
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
| `projectId` | string | yes | Galileo project UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "createdByUser": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen"
      },
      "hasUserCreatedSessions": true,
      "id": "string",
      "name": "Ava Chen",
      "numSpans": 1,
      "numTraces": 1,
      "projectId": "string",
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
| `createdBy` | string |  |
| `createdByUser.email` | string |  |
| `createdByUser.firstName` | string |  |
| `createdByUser.id` | string |  |
| `createdByUser.lastName` | string |  |
| `hasUserCreatedSessions` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `numSpans` | number |  |
| `numTraces` | number |  |
| `projectId` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Galileo API, this operation is `GET /v2/projects/:project_id/log_streams` (base URL `https://api.galileo.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-log-streams.md) for the provider-specific parameters and requirements.

