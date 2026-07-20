# SweetProcess: List Taskinstances

Retrieves task instances from SweetProcess.

```
GET https://connect.mindcloud.co/v1/universal/sweetProcess/latest/actions/list-taskinstances
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SweetProcess `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sweetProcess/latest/actions/list-taskinstances?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sweetProcess/latest/actions/list-taskinstances?${params}`, {
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
| `templateId` | number | no | Filter task instances belonging to the given task template. |
| `userUrl` | string | no | Filter tasks assigned to the given user API URL. |
| `contentType` | string | no | Filter tasks for a specific document type such as procedure or process. |
| `objectId` | number | no | Filter tasks for the referenced document ID. |
| `completed` | boolean | no | Return only completed or incomplete task instances. |
| `dueGte` | date | no | Lower bound for due date filtering in ISO 8601 format. Example: `2025-05-01`. |
| `dueLte` | date | no | Upper bound for due date filtering in ISO 8601 format. Example: `2025-05-31`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "progress": {},
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | The numeric SweetProcess task instance ID. |
| `name` | string | The task instance name. |
| `progress` | object | Task progress metadata, including completion details and step progress. |
| `url` | string | The API URL for the task instance. |

## Native endpoint

Through the native SweetProcess API, this operation is `GET /taskinstances/` (base URL `https://www.sweetprocess.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-taskinstances.md) for the provider-specific parameters and requirements.

