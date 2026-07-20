# Wrike: List Task Dependencies

Finds dependencies for a Wrike task.

```
GET https://connect.mindcloud.co/v1/universal/wrike/latest/actions/list-task-dependencies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wrike `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wrike/latest/actions/list-task-dependencies?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wrike/latest/actions/list-task-dependencies?${params}`, {
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
| `taskId` | string | yes | Wrike task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "lagTime": 1,
      "predecessorId": "string",
      "relationType": "string",
      "successorId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `lagTime` | number |  |
| `predecessorId` | string |  |
| `relationType` | string |  |
| `successorId` | string |  |

## Native endpoint

Through the native Wrike API, this operation is `GET /tasks/:taskId/dependencies` (base URL `https://{{credentials.accessTokenRequest.host}}/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-task-dependencies.md) for the provider-specific parameters and requirements.

