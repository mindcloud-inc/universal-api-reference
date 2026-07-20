# Zoho Projects: Delete Task List

Deletes an existing task list from Zoho Projects.

```
DELETE https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/delete-task-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Projects `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/delete-task-list?connectionId=$CONNECTION_ID&portalId=string&projectId=string&tasklistId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "portalId": "string",
  "projectId": "string",
  "tasklistId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/delete-task-list?${params}`, {
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
| `portalId` | string | yes | Portal identifier from Zoho Projects. |
| `projectId` | string | yes | Project identifier from Zoho Projects. |
| `tasklistId` | string | yes | Task list identifier from Zoho Projects. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zoho Projects API returns.

## Native endpoint

Through the native Zoho Projects API, this operation is `DELETE /portal/[:PORTALID]/projects/[:PROJECTID]/tasklists/[:TASKLISTID]` (base URL `https://projectsapi.zoho.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-task-list.md) for the provider-specific parameters and requirements.

