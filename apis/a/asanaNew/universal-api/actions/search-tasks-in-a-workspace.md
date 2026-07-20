# Asana: Search tasks in a workspace

Finds tasks in an Asana workspace.

```
GET https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/search-tasks-in-a-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/search-tasks-in-a-workspace?connectionId=$CONNECTION_ID&workspaceGid=string&workspace_guid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceGid": "string",
  "workspace_guid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/search-tasks-in-a-workspace?${params}`, {
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
| `text` | string | no | Performs a full-text search on both task name and description. |
| `optFields[]` | array<string> | no | This endpoint returns a compact resource, excluding most properties by default. To include properties, set this query parameter to a comma-separated list of the properties you wish to include. Accepts multiple values as an array. Default: `name,memberships,memberships.project,memberships.project.name,memberships.section,memberships.section.name,completed,notes,dependencies,due_on,external,num_subtasks,parent,permalink_url,custom_fields,custom_fields.enum_value,custom_fields.enum_value.name`. |
| `workspaceGid` | string | yes | Path parameter: workspace_gid |
| `workspace_guid` | string | yes | Globally unique identifier for the workspace or organization. |
| `projects.any` | string | no | Comma-separated list of project IDs. When paired with Search, returns tasks in Any of the provided Project IDs. |
| `projectsAny` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Asana API returns.

## Native endpoint

Through the native Asana API, this operation is `GET workspaces/:workspace_gid/tasks/search` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-tasks-in-a-workspace.md) for the provider-specific parameters and requirements.

