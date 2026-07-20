# Release0: Create Workspace

Creates a new workspace in Release0.

```
POST https://connect.mindcloud.co/v1/universal/release0/latest/actions/create-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Release0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/release0/latest/actions/create-workspace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/release0/latest/actions/create-workspace', {
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
| `name` | string | yes | The workspace name. |
| `slug` | string | no | The workspace slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chatUsage": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isPastDue": true,
      "isSuspended": true,
      "lastActivityAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "plan": "string",
      "slug": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chatUsage` | number |  |
| `createdAt` | date |  |
| `id` | string |  |
| `isPastDue` | boolean |  |
| `isSuspended` | boolean |  |
| `lastActivityAt` | date |  |
| `name` | string |  |
| `plan` | string |  |
| `slug` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Release0 API, this operation is `POST /v1/workspaces` (base URL `https://release0.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-workspace.md) for the provider-specific parameters and requirements.

