# SWELLEnterprise: Create Revision Request

Creates a revision request in SWELLEnterprise.

```
POST https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/create-revision-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SWELLEnterprise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/create-revision-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/create-revision-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes | The ID of the project. |
| `title` | string | yes | The revision request title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approval_id": 1,
      "assigned_to_user_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "due_date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "project_id": 1,
      "requested_by_user_id": 1,
      "requested_by": {
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen"
      },
      "revision_round": 1,
      "status": "string",
      "tenant_id": 1,
      "title": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approval_id` | number |  |
| `assigned_to_user_id` | number |  |
| `created_at` | date |  |
| `description` | string |  |
| `due_date` | date |  |
| `id` | number |  |
| `project_id` | number |  |
| `requested_by_user_id` | number |  |
| `requested_by.email` | string |  |
| `requested_by.id` | number |  |
| `requested_by.name` | string |  |
| `revision_round` | number |  |
| `status` | string |  |
| `tenant_id` | number |  |
| `title` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native SWELLEnterprise API, this operation is `POST /projects/projects/:project_id/revision-requests` (base URL `https://dashboard.swellsystem.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-revision-request.md) for the provider-specific parameters and requirements.

