# Galileo: Search Log Streams

Finds log streams in a Galileo project by filters.

```
GET https://connect.mindcloud.co/v1/universal/galileo/latest/actions/search-log-streams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Galileo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/galileo/latest/actions/search-log-streams?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/galileo/latest/actions/search-log-streams?${params}`, {
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
      "limit": 1,
      "logStreams": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "createdBy": "string",
          "createdByUser": {},
          "hasUserCreatedSessions": true,
          "id": "string",
          "name": "Ava Chen",
          "numSpans": 1,
          "numTraces": 1,
          "projectId": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ],
      "nextStartingToken": 1,
      "paginated": true,
      "startingToken": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `limit` | number |  |
| `logStreams` | array<object> |  |
| `logStreams[].createdAt` | date |  |
| `logStreams[].createdBy` | string |  |
| `logStreams[].createdByUser` | object |  |
| `logStreams[].hasUserCreatedSessions` | boolean |  |
| `logStreams[].id` | string |  |
| `logStreams[].name` | string |  |
| `logStreams[].numSpans` | number |  |
| `logStreams[].numTraces` | number |  |
| `logStreams[].projectId` | string |  |
| `logStreams[].updatedAt` | date |  |
| `nextStartingToken` | number |  |
| `paginated` | boolean |  |
| `startingToken` | number |  |

## Native endpoint

Through the native Galileo API, this operation is `POST /v2/projects/:project_id/log_streams/search` (base URL `https://api.galileo.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-log-streams.md) for the provider-specific parameters and requirements.

