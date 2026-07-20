# Yousign: Get Default Workspace

Retrieves the default workspace from Yousign.

```
GET https://connect.mindcloud.co/v1/universal/yousign/latest/actions/get-default-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yousign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yousign/latest/actions/get-default-workspace?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yousign/latest/actions/get-default-workspace?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "default": true,
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "externalName": "Ava Chen",
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "users": [
        {
          "id": "string"
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
| `createdAt` | date | Workspace creation timestamp. |
| `default` | boolean | Whether this is the default workspace. |
| `deletedAt` | date | Workspace deletion timestamp, when present. |
| `externalName` | string | External workspace name, when present. |
| `id` | string | Workspace ID. |
| `name` | string | Workspace name. |
| `updatedAt` | date | Workspace last update timestamp. |
| `users[].id` | string | User ID associated with the workspace. |

## Native endpoint

Through the native Yousign API, this operation is `GET /workspaces/default` (base URL `https://api-sandbox.yousign.app/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-default-workspace.md) for the provider-specific parameters and requirements.

