# Cirra: Archive Thread

Archives an existing Cirra thread by thread ID.

```
PUT https://connect.mindcloud.co/v1/universal/cirra/latest/actions/archive-thread
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cirra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cirra/latest/actions/archive-thread" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "threadId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cirra/latest/actions/archive-thread', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "threadId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `threadId` | list | yes | The thread ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archivedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "projectId": "string",
      "status": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archivedAt` | date |  |
| `createdAt` | date |  |
| `id` | string |  |
| `projectId` | string |  |
| `status` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Cirra API, this operation is `PUT /v1/cirra/threads/:threadId/archive` (base URL `http://api-public:9801`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/archive-thread.md) for the provider-specific parameters and requirements.

