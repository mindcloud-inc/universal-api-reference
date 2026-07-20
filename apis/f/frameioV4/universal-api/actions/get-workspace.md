# Frame.io v4: Get Workspace

Retrieves a workspace from Frame.io v4.

```
GET https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/get-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frame.io v4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/get-workspace?connectionId=$CONNECTION_ID&accountId=string&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/get-workspace?${params}`, {
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
| `accountId` | string | yes |  |
| `workspaceId` | string | yes |  |
| `include` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creator": {
        "active": true,
        "adobeUserId": "string",
        "avatarUrl": "https://example.com",
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string | Account ID |
| `createdAt` | date | Created Timestamp |
| `creator` | object | User details |
| `creator.active` | boolean | User active status |
| `creator.adobeUserId` | string | Adobe user ID |
| `creator.avatarUrl` | string | User avatar image url |
| `creator.email` | string | User email |
| `creator.id` | string | User ID - can be null for invited users with no frame account |
| `creator.name` | string | User name |
| `id` | string | Workspace ID |
| `name` | string | Workspace Name |
| `updatedAt` | date | Updated Timestamp |

## Native endpoint

Through the native Frame.io v4 API, this operation is `GET /accounts/:accountId/workspaces/:workspaceId` (base URL `https://api.frame.io/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace.md) for the provider-specific parameters and requirements.

