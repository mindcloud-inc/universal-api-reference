# Anthropic: Create Workspace Member

Adds a member to an Anthropic workspace.

```
POST https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/create-workspace-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anthropic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/create-workspace-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "userId": "string",
  "workspaceRole": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/create-workspace-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "userId": "string",
    "workspaceRole": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | string | yes | Workspace ID where member will be added. |
| `userId` | string | yes | User ID to add as member. |
| `workspaceRole` | string | yes | Role to grant in workspace. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "type": "string",
      "userId": "string",
      "workspaceId": "string",
      "workspaceRole": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `type` | string | Object type. |
| `userId` | string | User ID. |
| `workspaceId` | string | Workspace ID. |
| `workspaceRole` | string | Workspace role. |

## Native endpoint

Through the native Anthropic API, this operation is `POST /v1/organizations/workspaces/{workspace_id}/members` (base URL `https://api.anthropic.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-workspace-member.md) for the provider-specific parameters and requirements.

