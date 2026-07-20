# Clockify: Create Workspace Client

Creates a new workspace client in Clockify.

```
POST https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-workspace-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-workspace-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-workspace-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | list<string> | yes | Workspace identifier. |
| `name` | string | yes | Client name. |
| `email` | string | no | Client email. |
| `address` | string | no | Client address. |
| `note` | string | no | Client note. |

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
| `address` | string |  |
| `archived` | boolean |  |
| `ccEmails` | array<string> |  |
| `currencyCode` | string |  |
| `currencyId` | string |  |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |
| `note` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `POST workspaces/:workspaceId/clients` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-workspace-client.md) for the provider-specific parameters and requirements.

