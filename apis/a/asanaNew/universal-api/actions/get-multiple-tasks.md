# Asana: Get multiple tasks

Retrieves tasks from Asana.

```
GET https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-multiple-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-multiple-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-multiple-tasks?${params}`, {
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
| `assignee` | string | no |  |
| `completedSince` | date | no |  |
| `limit` | number | no |  |
| `modifiedSince` | date | no |  |
| `offset` | string | no |  |
| `optFields[]` | array<string> | no |  |
| `project` | string | no |  |
| `section` | string | no |  |
| `workspace` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "gid": "string",
      "name": "Ava Chen",
      "resourceSubtype": "string",
      "resourceType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `gid` | string |  |
| `name` | string |  |
| `resourceSubtype` | string |  |
| `resourceType` | string |  |

## Native endpoint

Through the native Asana API, this operation is `GET tasks` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-multiple-tasks.md) for the provider-specific parameters and requirements.

