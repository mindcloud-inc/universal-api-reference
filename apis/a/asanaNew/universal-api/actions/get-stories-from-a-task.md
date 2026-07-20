# Asana: Get stories from a task

Retrieves stories for a task from Asana.

```
GET https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-stories-from-a-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-stories-from-a-task?connectionId=$CONNECTION_ID&limit=25&offset=0&taskGid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "taskGid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-stories-from-a-task?${params}`, {
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
| `limit` | number | no |  |
| `offset` | string | no |  |
| `optFields[]` | array<string> | no | This endpoint returns a compact resource, excluding most properties by default. To include additional properties in the response add them here. Default: `text,created_by.name,created_at,resource_type,resource_subtype`. |
| `taskGid` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {
        "gid": "string",
        "name": "Ava Chen",
        "resourceType": "string"
      },
      "gid": "string",
      "resourceSubtype": "string",
      "resourceType": "string",
      "text": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `createdBy.gid` | string |  |
| `createdBy.name` | string |  |
| `createdBy.resourceType` | string |  |
| `gid` | string |  |
| `resourceSubtype` | string |  |
| `resourceType` | string |  |
| `text` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Asana API, this operation is `GET tasks/:task_gid/stories` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-stories-from-a-task.md) for the provider-specific parameters and requirements.

