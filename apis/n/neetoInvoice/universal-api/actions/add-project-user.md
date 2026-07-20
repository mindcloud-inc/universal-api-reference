# NeetoInvoice: Add Project User

Adds a user to a project in NeetoInvoice.

```
POST https://connect.mindcloud.co/v1/universal/neetoInvoice/latest/actions/add-project-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeetoInvoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/neetoInvoice/latest/actions/add-project-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neetoInvoice/latest/actions/add-project-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | no | Project identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "projectUser": {
        "id": "string",
        "projectId": "string",
        "role": "string",
        "userId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `projectUser.id` | string |  |
| `projectUser.projectId` | string |  |
| `projectUser.role` | string |  |
| `projectUser.userId` | string |  |

## Native endpoint

Through the native NeetoInvoice API, this operation is `POST /projects/{project_id}/project_users` (base URL `https://{{credentials.workspaceSubdomain}}.neetoinvoice.com/api/external/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-project-user.md) for the provider-specific parameters and requirements.

