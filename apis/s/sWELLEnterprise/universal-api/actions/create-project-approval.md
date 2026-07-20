# SWELLEnterprise: Create Project Approval

Creates a project approval in SWELLEnterprise.

```
POST https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/create-project-approval
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SWELLEnterprise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/create-project-approval" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/create-project-approval', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes | The ID of the project. |
| `type` | string | yes | Approval type. Runtime evidence verified final for this account. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comments": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "project_id": 1,
      "project": {
        "approval_status": "string",
        "id": 1,
        "name": "Ava Chen"
      },
      "requested_by_user_id": 1,
      "requested_by": {
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen"
      },
      "status": "string",
      "tenant_id": 1,
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments` | string |  |
| `created_at` | date |  |
| `id` | number |  |
| `project_id` | number |  |
| `project.approval_status` | string |  |
| `project.id` | number |  |
| `project.name` | string |  |
| `requested_by_user_id` | number |  |
| `requested_by.email` | string |  |
| `requested_by.id` | number |  |
| `requested_by.name` | string |  |
| `status` | string |  |
| `tenant_id` | number |  |
| `type` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native SWELLEnterprise API, this operation is `POST /projects/projects/:project_id/approvals` (base URL `https://dashboard.swellsystem.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project-approval.md) for the provider-specific parameters and requirements.

