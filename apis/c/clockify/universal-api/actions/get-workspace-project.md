# Clockify: Get Workspace Project

Retrieves a specific workspace project from Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-workspace-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-workspace-project?connectionId=$CONNECTION_ID&workspaceId=string&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-workspace-project?${params}`, {
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
| `workspaceId` | list<string> | yes | Workspace identifier. |
| `projectId` | string | yes | Project identifier. |
| `hydrated` | boolean | no | Include hydrated project data. |
| `customFieldEntityType` | string | no | Custom field entity type filter. |
| `expenseLimit` | number | no | Maximum expenses to include. |
| `expenseDate` | string | no | Include expenses before this date (yyyy-MM-dd). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "billable": true,
      "clientId": "string",
      "color": "string",
      "duration": "string",
      "id": "string",
      "name": "Ava Chen",
      "note": "string",
      "public": true,
      "template": true,
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `billable` | boolean |  |
| `clientId` | string |  |
| `color` | string |  |
| `duration` | string |  |
| `id` | string |  |
| `name` | string |  |
| `note` | string |  |
| `public` | boolean |  |
| `template` | boolean |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `GET workspaces/:workspaceId/projects/:projectId` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace-project.md) for the provider-specific parameters and requirements.

