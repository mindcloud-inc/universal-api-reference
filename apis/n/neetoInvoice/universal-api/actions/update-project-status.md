# NeetoInvoice: Update Project Status

Updates a project status in NeetoInvoice.

```
PUT https://connect.mindcloud.co/v1/universal/neetoInvoice/latest/actions/update-project-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeetoInvoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/neetoInvoice/latest/actions/update-project-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neetoInvoice/latest/actions/update-project-status', {
  method: 'PUT',
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
| `projectId` | string | no | Project identifier whose status will be updated. |
| `status` | string | no | New project status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "project": {
        "id": "string",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `project.id` | string |  |
| `project.status` | string |  |

## Native endpoint

Through the native NeetoInvoice API, this operation is `POST /projects/update_status` (base URL `https://{{credentials.workspaceSubdomain}}.neetoinvoice.com/api/external/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project-status.md) for the provider-specific parameters and requirements.

