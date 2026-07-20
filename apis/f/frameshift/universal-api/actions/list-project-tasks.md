# Frameshift: List Project Tasks

Retrieves a list of project tasks from Frameshift.

```
GET https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/list-project-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frameshift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/list-project-tasks?connectionId=$CONNECTION_ID&project_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/list-project-tasks?${params}`, {
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
| `project_id` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Frameshift API returns.

## Native endpoint

Through the native Frameshift API, this operation is `GET /v1/projects/:project_id/tasks` (base URL `https://mosaic.frameshift.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-tasks.md) for the provider-specific parameters and requirements.

