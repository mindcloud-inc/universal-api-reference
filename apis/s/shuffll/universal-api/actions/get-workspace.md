# Shuffll: Get Workspace

Retrieves a workspace from Shuffll by ID.

```
GET https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/get-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shuffll `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/get-workspace?connectionId=$CONNECTION_ID&organizationId=69cac8104c4a701fd26271a1&workspaceId=69cac8104c4a701fd26271a5" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "69cac8104c4a701fd26271a1",
  "workspaceId": "69cac8104c4a701fd26271a5"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/get-workspace?${params}`, {
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
| `organizationId` | string | yes | Shuffll organization id. Default: `69cac8104c4a701fd26271a1`. |
| `workspaceId` | string | yes | Shuffll workspace id. Default: `69cac8104c4a701fd26271a5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assetCount": 1,
      "branding": {},
      "createdByEmail": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "projectCount": 1,
      "templateCount": 1,
      "userCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assetCount` | number | Asset count. |
| `branding` | object | Workspace branding. |
| `createdByEmail` | string | Creator email. |
| `id` | string | Workspace id. |
| `name` | string | Workspace name. |
| `projectCount` | number | Project count. |
| `templateCount` | number | Template count. |
| `userCount` | number | Workspace user count. |

## Native endpoint

Through the native Shuffll API, this operation is `GET /auth/organization/:organizationId/workspace/:workspaceId` (base URL `https://api.shuffll.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace.md) for the provider-specific parameters and requirements.

