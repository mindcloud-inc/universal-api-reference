# Anthropic: Create Workspace

Creates a workspace in the Anthropic organization.

```
POST https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/create-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anthropic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/create-workspace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/create-workspace', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Display name for the new workspace. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archivedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dataResidency": {},
      "displayColor": "string",
      "id": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archivedAt` | date | Workspace archive timestamp. |
| `createdAt` | date | Workspace creation timestamp. |
| `dataResidency` | object | Data residency settings. |
| `displayColor` | string | Workspace display color. |
| `id` | string | Workspace ID. |
| `name` | string | Workspace name. |
| `type` | string | Object type. |

## Native endpoint

Through the native Anthropic API, this operation is `POST /v1/organizations/workspaces` (base URL `https://api.anthropic.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-workspace.md) for the provider-specific parameters and requirements.

