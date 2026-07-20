# Dremio: Get Maintenance Task

Retrieves a maintenance task from a Dremio project.

```
GET https://connect.mindcloud.co/v1/universal/dremio/latest/actions/get-maintenance-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dremio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dremio/latest/actions/get-maintenance-task?connectionId=$CONNECTION_ID&projectId=string&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dremio/latest/actions/get-maintenance-task?${params}`, {
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
| `projectId` | string | yes |  |
| `taskId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config": {},
      "id": "string",
      "isEnabled": true,
      "level": "string",
      "sourceName": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config` | object |  |
| `id` | string |  |
| `isEnabled` | boolean |  |
| `level` | string |  |
| `sourceName` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Dremio API, this operation is `GET /projects/:project_id/maintenance/tasks/:taskId` (base URL `https://api.dremio.cloud/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-maintenance-task.md) for the provider-specific parameters and requirements.

