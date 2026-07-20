# Clockify: List Workspace Clients

Lists all workspace clients in Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-workspace-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-workspace-clients?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-workspace-clients?${params}`, {
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
| `name` | string | no | Filter clients by name. |
| `archived` | boolean | no | Include archived clients. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "archived": true,
      "ccEmails": {},
      "currencyCode": "string",
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
| `address` | object |  |
| `archived` | boolean |  |
| `ccEmails` | object |  |
| `currencyCode` | string |  |
| `currencyId` | string |  |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |
| `note` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `GET workspaces/:workspaceId/clients` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-workspace-clients.md) for the provider-specific parameters and requirements.

