# Clockify: Update Workspace Client

Updates an existing workspace client in Clockify.

```
PUT https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-workspace-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-workspace-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-workspace-client', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | list<string> | yes | Workspace identifier. |
| `id` | string | yes | Client identifier. |
| `name` | string | no | Client name. |
| `email` | string | no | Client email. |
| `address` | string | no | Client address. |
| `note` | string | no | Client note. |
| `archived` | boolean | no | Archive state. |
| `ccEmails[]` | array<string> | no | Additional invoice emails. |
| `currencyId` | string | no | Currency identifier. |
| `archiveProjects` | boolean | no | Archive related projects. |
| `markTasksAsDone` | boolean | no | Mark tasks as done when archiving. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "archived": true,
      "ccEmails": [
        "ava@example.com"
      ],
      "currencyId": "string",
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "note": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `archived` | boolean |  |
| `ccEmails` | array<string> |  |
| `currencyId` | string |  |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |
| `note` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `PUT workspaces/:workspaceId/clients/:id` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-workspace-client.md) for the provider-specific parameters and requirements.

