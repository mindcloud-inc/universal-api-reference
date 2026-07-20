# Planfix: List Tasks

Retrieves tasks from Planfix.

```
GET https://connect.mindcloud.co/v1/universal/planfix/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planfix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planfix/latest/actions/list-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planfix/latest/actions/list-tasks?${params}`, {
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
| `fields` | string | no | Comma-separated task fields to return, for example id,name,description. Default: `id,name,description`. Example: `id,name,description`. |
| `pageSize` | number | no | Number of tasks to return per request. Planfix allows 1 to 100. Default: `100`. Example: `1`. |
| `offset` | number | no | Zero-based offset from the beginning of the task list. Default: `0`. Example: `0`. |
| `filterId` | string | no | Optional Planfix task filter ID, for example out. Example: `out`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `runAsUserId` | string | no | Run the request on behalf of a specific employee or contact, for example user:2. Admin-only. Example: `user:2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native Planfix API, this operation is `POST /task/list` (base URL `{{credentials.accountBaseUrl}}/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

