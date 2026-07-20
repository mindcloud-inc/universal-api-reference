# NeetoInvoice: List Project Users

Retrieves all project users from NeetoInvoice.

```
GET https://connect.mindcloud.co/v1/universal/neetoInvoice/latest/actions/list-project-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeetoInvoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neetoInvoice/latest/actions/list-project-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neetoInvoice/latest/actions/list-project-users?${params}`, {
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
| `projectId` | string | no | Project identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "projectUsers": [
        {
          "id": "string",
          "projectId": "string",
          "role": "string",
          "userId": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `projectUsers[].id` | string |  |
| `projectUsers[].projectId` | string |  |
| `projectUsers[].role` | string |  |
| `projectUsers[].userId` | string |  |

## Native endpoint

Through the native NeetoInvoice API, this operation is `GET /projects/{project_id}/project_users` (base URL `https://{{credentials.workspaceSubdomain}}.neetoinvoice.com/api/external/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-users.md) for the provider-specific parameters and requirements.

