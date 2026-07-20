# Taskade: List Folder Projects

Retrieves projects from a Taskade folder.

```
GET https://connect.mindcloud.co/v1/universal/taskade/latest/actions/list-folder-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Taskade `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/taskade/latest/actions/list-folder-projects?connectionId=$CONNECTION_ID&folderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/taskade/latest/actions/list-folder-projects?${params}`, {
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
| `folderId` | string | yes | Folder ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Taskade API returns.

## Native endpoint

Through the native Taskade API, this operation is `GET /folders/:folderId/projects` (base URL `https://www.taskade.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-folder-projects.md) for the provider-specific parameters and requirements.

